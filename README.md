# Google Generative AI SDK for Dart

The Google Generative AI SDK for Dart allows developers to use state-of-the-art
Large Language Models (LLMs) to build language applications.

## Getting Started

This repository contains a few sample apps. To try them out, follow these
steps:

- Change directory to the samples package.
- Export a `$GOOGLE_API_KEY` environment variable with an API key with access to
  the Gemini generative models, or run the below commands with an environment
  containing this variable.
- Run any sample from the `bin` directory. `dart bin/simple_text.dart`.

## Using the SDK in your own app

Add a dependency on this repository to the path `pkgs/google_generative_ai`.
Once the API is stable the package will be available from pub.
We welcome pre-publish feedback through GitHub issues.

```yaml
dependencies:
  google_generative_ai:
    git:
      url: git@github.com:google/generative-ai-dart.git
      path: pkgs/google_generative_ai
      ref: main
```

### Initializing the API client

```dart
  final model = GenerativeModel(model: 'gemini-pro', apiKey: apiKey);
```

### Calling the API

```dart
  final prompt = 'Write a story about a magic backpack.';
  final content = [Content.text(prompt)];
  final response = await model.generateContent(content);
  print(response.text);
```

## Documentation

TODO: Update documentation and add link.

## Contributing

See [Contributing](docs/CONTRIBUTING.md) for more information on contributing to
the Generative AI SDK for Dart.

## License

The contents of this repository are licensed under the
[Apache License, version 2.0](http://www.apache.org/licenses/LICENSE-2.0).