---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173220"
---
# <span data-ttu-id="7bfcd-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7bfcd-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="7bfcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bfcd-102">SYNOPSIS</span></span>
<span data-ttu-id="7bfcd-103">Exportiert das Webdienstdefinitionsobjekt als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="7bfcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bfcd-104">SYNTAX</span></span>

### <span data-ttu-id="7bfcd-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="7bfcd-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bfcd-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="7bfcd-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bfcd-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bfcd-107">DESCRIPTION</span></span>
<span data-ttu-id="7bfcd-108">Exportiert das Definitionsobjekt für den angegebenen Webdienst als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="7bfcd-109">Sie können die Zeichenfolge sofort zurückgeben oder in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="7bfcd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7bfcd-110">EXAMPLES</span></span>

### <span data-ttu-id="7bfcd-111">Beispiel 1: Exportieren als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="7bfcd-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="7bfcd-112">Beispiel 2: Exportieren in eine Datei</span><span class="sxs-lookup"><span data-stu-id="7bfcd-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="7bfcd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bfcd-113">PARAMETERS</span></span>

### <span data-ttu-id="7bfcd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bfcd-114">-DefaultProfile</span></span>
<span data-ttu-id="7bfcd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7bfcd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7bfcd-116">-Force</span></span>
<span data-ttu-id="7bfcd-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-117">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7bfcd-118">-OutputFile</span></span>
<span data-ttu-id="7bfcd-119">Der Dateipfad für die exportierte Definition.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-119">The file path for exported definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="7bfcd-120">-ToJsonString</span></span>
<span data-ttu-id="7bfcd-121">Gibt an, dass die Definition als eine JSON-Zeichenfolge exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToJSON
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="7bfcd-122">-WebService</span></span>
<span data-ttu-id="7bfcd-123">Das zu exportierende Webdienstdefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-123">The web service definition object to be exported.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bfcd-124">-Confirm</span></span>
<span data-ttu-id="7bfcd-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7bfcd-126">-WhatIf</span></span>
<span data-ttu-id="7bfcd-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bfcd-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bfcd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bfcd-129">CommonParameters</span></span>
<span data-ttu-id="7bfcd-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bfcd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bfcd-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bfcd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bfcd-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7bfcd-132">INPUTS</span></span>

### <span data-ttu-id="7bfcd-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="7bfcd-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7bfcd-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7bfcd-134">OUTPUTS</span></span>

### <span data-ttu-id="7bfcd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7bfcd-135">System.String</span></span>

## <span data-ttu-id="7bfcd-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7bfcd-136">NOTES</span></span>
<span data-ttu-id="7bfcd-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7bfcd-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7bfcd-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7bfcd-138">RELATED LINKS</span></span>
