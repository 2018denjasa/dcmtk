# declare project
project(dcmect)

# declare include directories which hold for all subdirectories
include_directories("${dcmect_SOURCE_DIR}/include" "${dcmfg_SOURCE_DIR}/include" "${dcmiod_SOURCE_DIR}/include" "${dcmdata_SOURCE_DIR}/include" "${ofstd_SOURCE_DIR}/include" "${oflog_SOURCE_DIR}/include" ${ZLIB_INCDIR})

# recurse into subdirectories
foreach(SUBDIR libsrc include tests)
  add_subdirectory(${SUBDIR})
endforeach()
