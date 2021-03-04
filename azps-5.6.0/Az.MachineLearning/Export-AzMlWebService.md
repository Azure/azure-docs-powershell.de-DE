---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 0fad6a81f895643f8783ca8d179d68e31eed6da7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931011"
---
# <span data-ttu-id="28355-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="28355-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="28355-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28355-102">SYNOPSIS</span></span>
<span data-ttu-id="28355-103">Exportiert das Webdienstdefinitionsobjekt als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="28355-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="28355-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28355-104">SYNTAX</span></span>

### <span data-ttu-id="28355-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="28355-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28355-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="28355-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28355-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28355-107">DESCRIPTION</span></span>
<span data-ttu-id="28355-108">Exportiert das Definitionsobjekt für den angegebenen Webdienst als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="28355-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="28355-109">Sie können die Zeichenfolge sofort zurückgeben oder in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="28355-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="28355-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28355-110">EXAMPLES</span></span>

### <span data-ttu-id="28355-111">Beispiel 1: Exportieren als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="28355-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="28355-112">Beispiel 2: Exportieren in eine Datei</span><span class="sxs-lookup"><span data-stu-id="28355-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="28355-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28355-113">PARAMETERS</span></span>

### <span data-ttu-id="28355-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28355-114">-DefaultProfile</span></span>
<span data-ttu-id="28355-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="28355-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28355-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="28355-116">-Force</span></span>
<span data-ttu-id="28355-117">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="28355-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="28355-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="28355-118">-OutputFile</span></span>
<span data-ttu-id="28355-119">Der Dateipfad für die exportierte Definition.</span><span class="sxs-lookup"><span data-stu-id="28355-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="28355-120">-ToJsonString</span><span class="sxs-lookup"><span data-stu-id="28355-120">-ToJsonString</span></span>
<span data-ttu-id="28355-121">Gibt an, dass die Definition als JSON-Zeichenfolge exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="28355-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="28355-122">-WebService</span><span class="sxs-lookup"><span data-stu-id="28355-122">-WebService</span></span>
<span data-ttu-id="28355-123">Das webdienstdefinitionsobjekt, das exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="28355-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="28355-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28355-124">-Confirm</span></span>
<span data-ttu-id="28355-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28355-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28355-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28355-126">-WhatIf</span></span>
<span data-ttu-id="28355-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28355-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28355-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28355-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28355-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28355-129">CommonParameters</span></span>
<span data-ttu-id="28355-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28355-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28355-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28355-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28355-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28355-132">INPUTS</span></span>

### <span data-ttu-id="28355-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="28355-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="28355-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28355-134">OUTPUTS</span></span>

### <span data-ttu-id="28355-135">System.String</span><span class="sxs-lookup"><span data-stu-id="28355-135">System.String</span></span>

## <span data-ttu-id="28355-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="28355-136">NOTES</span></span>
<span data-ttu-id="28355-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="28355-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="28355-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="28355-138">RELATED LINKS</span></span>
