#!/bin/bash

# Set the source and destination directories
source_dir="./githooks/"
dest_dir="./.git/hooks/"
excluded_file="run"

# Loop through all files in the source directory
for file in "${source_dir}"*; do

  # Check if the current file is excluded file
  if [[ "${file}" == "${source_dir}${excluded_file}" ]]; then
    # Skip this file if it's excluded file
    continue
  fi

  # Copy the file to the destination directory
  cp "${file}" "${dest_dir}"

  # Make the copied file executable
  chmod +x "${dest_dir}${file##*/}"

done