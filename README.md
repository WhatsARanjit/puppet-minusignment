minusignment
-----
Removes a value from an attribute if it exists.

For example for the resource:

    example_resource { 'example_resource_instance':
        param => [ 'param_value1', 'param_value2' ],
    }

    minusignment(example_resource['example_resource_instance'], 'param', 'param_value2')

    Would return:
    Example_resource { 'example_resource_instance':
        param => [ 'param_value1' ],
    }

    minusignment(example_resource['example_resource_instance'], 'param', 'param_notused')

    Would return:
    Example_resource { 'example_resource_instance':
        param => [ 'param_value1', 'param_value2' ],
    }
