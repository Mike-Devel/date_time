cmake_minimum_required(VERSION 3.8)
project(boost-date_time LANGUAGES CXX)

add_library(boost_date_time INTERFACE)
add_library(Boost::date_time ALIAS boost_date_time)

target_include_directories(boost_date_time INTERFACE include)

target_link_libraries(boost_date_time
	INTERFACE
		Boost::algorithm
		Boost::assert
		Boost::config
		Boost::core
		Boost::io
		Boost::lexical_cast
		Boost::mpl
		Boost::numeric_conversion
		Boost::range
		Boost::serialization
		Boost::smart_ptr
		Boost::static_assert
		Boost::tokenizer
		Boost::type_traits
		Boost::utility
		Boost::winapi
)
