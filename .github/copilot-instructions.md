# Loloward Image Repository
Loloward is an image asset repository containing categorized image files for use in projects. The repository contains 66 images organized into 4 directories: animals, images, objects, and shapes.

**Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.**

## Repository Structure Overview
- **Repository Type**: Image/media asset collection (no build system or traditional code)
- **Total Assets**: 66 image files (~19MB total)
- **File Formats**: JPG (52 files), PNG (8 files), WEBP (2 files), JPEG (4 files)
- **Organization**: 4 main directories categorizing different types of images

## Working Effectively

### Repository Navigation and Exploration
- Always start by examining the repository structure: `ls -la`
- **Directory sizes (largest to smallest)**:
  - `images/` - 6.3MB (mixed content - duplicates some animal/object images)
  - `animals/` - 5.2MB (animal photographs)
  - `objects/` - 1.1MB (furniture, electronics, household items)
  - `shapes/` - 228KB (geometric shapes and simple graphics)

### File Operations
- **File search operations are FAST (< 0.01 seconds)**:
  - Search by extension: `find . -name "*.jpg" | wc -l`
  - Directory analysis: `du -sh */ | sort -hr`
  - File type analysis: `file animals/* | head -5`
- **Repository size check**: `du -s .` (completes in 0.002 seconds)

### Git Operations
- **Standard git operations work normally**:
  - Check status: `git status`
  - View history: `git log --oneline -10`
  - View branches: `git branch -a`
- **File management timing**: All git operations complete in < 1 second
- **NEVER** need extended timeouts - all operations are instant

## Repository Content Details

### Directory Contents
- **animals/**: Wildlife and pet photographs (18 images)
  - Formats: JPG, WEBP, JPEG
  - Size range: 19KB to 1.5MB per file
  - Examples: Camel, cats, dogs, birds, farm animals
  
- **images/**: Mixed image collection (27 images) 
  - Contains duplicates from other directories
  - All major formats represented
  
- **objects/**: Furniture and household items (11 images)
  - Focus on furniture (tables, chairs), electronics (TV)
  - Mostly JPG format
  
- **shapes/**: Simple graphics and geometric shapes (10 images)
  - Smallest files (1.7KB to 99KB)
  - Mix of PNG and JPG formats

### File Naming Conventions
- **Descriptive names**: Files use descriptive English names
- **Some international characters**: Arabic text in animal directory
- **Wikipedia-style naming**: Many files follow Wikipedia naming patterns
- **Numeric IDs**: Some files use numeric identifiers (e.g., "1000259982.png")

## Common Tasks

### Finding Specific Images
- **By category**: `ls animals/`, `ls objects/`, `ls shapes/`
- **By file type**: `find . -name "*.png"` or `find . -name "*.jpg"`
- **By size**: `ls -lhS animals/` (sort by size)
- **File information**: `file path/to/image.jpg` (shows dimensions, format details)

### Organizing and Managing Assets
- **Add new images**: Place in appropriate category directory
- **Check for duplicates**: The `images/` directory contains many duplicates from other directories
- **Validate file integrity**: Use `file` command to verify image formats
- **Repository space**: Monitor with `du -sh */` (completes instantly)

### Quality Assurance
- **File format validation**: `file animals/* | grep -v "JPEG\|PNG\|RIFF"` (find corrupted files)
- **Size analysis**: `find . -name "*.jpg" -size +1M` (find large files)
- **Name validation**: Look for files with special characters that might cause issues

## Validation Requirements
- **ALWAYS** verify new images open correctly using `file` command
- **ALWAYS** check file sizes are reasonable for their content type
- **ALWAYS** place images in appropriate category directories
- **ALWAYS** run `git status` after adding/modifying files
- **ALWAYS** ensure file names don't conflict with existing assets

## Tools Available
- **Git**: Full git functionality for version control
- **File utilities**: `ls`, `find`, `du`, `file`, `sort` all available
- **Text processing**: `grep`, `awk`, `head`, `tail`, `wc` available
- **NOT available**: ImageMagick, image editing tools
- **File operations**: All standard Unix file operations work instantly

## Performance Expectations
- **All operations complete in < 1 second** - no timeouts needed
- **Repository browsing**: Instant
- **File searches**: 0.005 seconds for full repository scan
- **Directory sizing**: 0.002 seconds
- **Git operations**: < 1 second for all standard operations

## Common Outputs Reference

### Repository root listing
```
$ ls -la
drwxr-xr-x 7 runner runner 4096 animals/
drwxrwxr-x 2 runner runner 4096 images/
drwxrwxr-x 2 runner runner 4096 objects/  
drwxrwxr-x 2 runner runner 4096 shapes/
```

### File format breakdown
```
$ find . -name "*.jpg" | wc -l && find . -name "*.png" | wc -l && find . -name "*.webp" | wc -l && find . -name "*.jpeg" | wc -l
52
8
2
4
```

### Directory sizes
```
$ du -sh */
6.3M	images/
5.2M	animals/
1.1M	objects/
228K	shapes/
```

## IMPORTANT NOTES
- **No build or test systems** - this is purely an asset repository
- **No timeouts needed** - all operations are instantaneous
- **Focus on organization** - primary concern is proper categorization of images
- **Duplicate management** - be aware that `images/` directory contains duplicates
- **International content** - some files have Arabic names, handle with care
