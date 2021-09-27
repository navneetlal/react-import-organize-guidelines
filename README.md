# Guidelines
Guidelines for organizing imports in reactjs

1. Grouping
    1. Imports from react/nextjs should be grouped under one.
        - example - `react`, `react-router`, `next`, `nextLink`, `useState`, `useReducer`, etc
    1. Any supporting libraries like `axios`, `xlsx`, `rxjs`, `bluebird`, etc should be grouped together.
    1. React components from external library like `@material-ui/core`, `@mui/material`, `antd`, `react-bootstrap`, etc should be groped next.
    1. Icon components from external library like `react-icons`, `@material-ui/icons`, `@mui/icons-material`, `@ant-design/icons` should be grouped next.
    1. Repeat step 3, 4 for the internal library.
    1. Imports from internal utils, libs should be grouped next
    1. Store, Actions, [Epics, Reducers], & Types should be grouped next in the same order.
    1. Any images, css, files, etc should be last to be imported and grouped in one.
1. Sorting
    1. Sort the imports in alphabetical order.
    1. Sorting should be per group.

> Note: NO comments in import statement


**Example:**
```ts
// External Libraries //
import React, { useEffect, useState } from 'react';
import { useDispatch, useSelector } from 'react-redux';

import axios from 'axios';
import { useFormikContext } from 'formik';
import { useKeycloak } from '@react-keycloak/ssr';

import Accordion from '@material-ui/core/Accordion';
import AccordionDetails from '@material-ui/core/AccordionDetails';
import AccordionSummary from '@material-ui/core/AccordionSummary';
import Grid from '@material-ui/core/Grid';
import Typography from '@material-ui/core/Typography';

import ChevronLeft from '@material-ui/icons/ChevronLeft';
import ExpandMoreIcon from '@material-ui/icons/ExpandMore';

import { makeStyles, useTheme } from '@material-ui/core/styles';

// Internal Libraries //
import Chip from '@common/chips/Chip';
import DropDown from '@common/autocomplete/Autocomplete';
import IconButton from '@common/iconButton/IconButton';
import TextBox from '@common/textbox/Textbox';

import AddIcon from '@common/icons/AddIcon';
import DeleteIcon from '@common/icons/DeleteIcon';
import SubtractIcon from '@common/icons/SubtractIcon';
import YellowFlag from '@common/icons/YellowFlag';

import type { RootState } from '@store/store';
import { addCustomer, addLocation, getLocation } from '@store/track-n-trace/actions';

import NewCustomer from '../components/Customer';
import NewLocation from '../components/Location';

import 'font-awesome/css/font-awesome.min.css';
import '../styles/globals.css';
```