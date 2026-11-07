# Imaging.Metadata

A .NET library for reading metadata from image files.

> **Status:** early development. The solution and test project are scaffolded, but the public API has not been implemented yet. This README describes the project's goals and layout, and will grow as features land.

## Goals

- Read camera and image metadata (EXIF and related tags) from common photo formats.
- Support both processed images (JPEG) and camera RAW files (NEF, DNG).
- Provide a simple, strongly typed API with no native dependencies.

## Requirements

- [.NET 10 SDK](https://dotnet.microsoft.com/download)

## Getting started

```powershell
git clone <repository-url>
cd Imaging.Metadata\Imaging.Metadata

dotnet build
dotnet test
```

## Project structure

```
Imaging.Metadata/
├── Imaging.Metadata.slnx            Solution file
├── Imaging.Metadata/                Class library (net10.0)
└── Imaging.Metadata.Tests/          xUnit test project
    └── test-images/                 Sample images from various cameras
```

## Testing

Tests use [xUnit](https://xunit.net/) with coverlet for code coverage. The `test-images` folder holds sample files from a range of manufacturers (Apple, Canon, Nikon, Olympus, Samsung, Light and others), in JPEG, NEF and DNG formats, to exercise real-world metadata variations.

Run all tests:

```powershell
dotnet test
```

Expected values can be cross-checked against [ExifTool](https://exiftool.org/).

## Contributing

Issues and pull requests are welcome. Please keep changes focused and include tests where behaviour changes.

## License

Licensed under the [Apache License 2.0](LICENSE).
