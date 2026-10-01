project(Allpass_assignment VERSION 0.0.1)
juce_add_console_app(Allpass_assignment PRODUCT_NAME "Allpass_assignment")
target_sources(Allpass_assignment PRIVATE main.cpp allpassfilter.cpp allpassfilter.h)
target_compile_definitions(Allpass_assignment PRIVATE JUCE_WEB_BROWSER=0 JUCE_USE_CURL=0)

target_link_libraries(Allpass_assignment
        PRIVATE
        juce::juce_audio_basics
        juce::juce_audio_devices
        juce::juce_audio_formats
        juce::juce_audio_processors

        PUBLIC
        juce::juce_recommended_config_flags
        juce::juce_recommended_warning_flags
)

target_compile_features(Allpass_assignment PRIVATE cxx_std_20)