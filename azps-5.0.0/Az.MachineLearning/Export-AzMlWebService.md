---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/export-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Export-AzMlWebService.md
ms.openlocfilehash: 3c1199967a462695cdabeb3113150f8b475812ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180323"
---
# <span data-ttu-id="2f0ec-101">Export-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="2f0ec-101">Export-AzMlWebService</span></span>

## <span data-ttu-id="2f0ec-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2f0ec-103">Exportiert das Web Service Definition-Objekt als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-103">Exports the web service definition object as a JSON formatted string.</span></span>

## <span data-ttu-id="2f0ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f0ec-104">SYNTAX</span></span>

### <span data-ttu-id="2f0ec-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="2f0ec-105">ExportToFile</span></span>
```
Export-AzMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f0ec-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="2f0ec-106">ExportToJSON</span></span>
```
Export-AzMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f0ec-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f0ec-107">DESCRIPTION</span></span>
<span data-ttu-id="2f0ec-108">Exportiert das Definitionsobjekt für den angegebenen Webdienst als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-108">Exports the definition object for the specified web service as a JSON formatted string.</span></span>
<span data-ttu-id="2f0ec-109">Sie können die Zeichenfolge sofort zurückgeben oder in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="2f0ec-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f0ec-110">EXAMPLES</span></span>

### <span data-ttu-id="2f0ec-111">Beispiel 1: Exportieren als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2f0ec-111">Example 1: Export as string</span></span>
```
Export-AzMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="2f0ec-112">Beispiel 2: Exportieren in eine Datei</span><span class="sxs-lookup"><span data-stu-id="2f0ec-112">Example 2: Export to file</span></span>
```
Export-AzMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="2f0ec-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f0ec-113">PARAMETERS</span></span>

### <span data-ttu-id="2f0ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f0ec-114">-DefaultProfile</span></span>
<span data-ttu-id="2f0ec-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2f0ec-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f0ec-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2f0ec-116">-Force</span></span>
<span data-ttu-id="2f0ec-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2f0ec-118">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="2f0ec-118">-OutputFile</span></span>
<span data-ttu-id="2f0ec-119">Der Dateipfad für die exportierte Definition.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="2f0ec-120">-Tojsonl</span><span class="sxs-lookup"><span data-stu-id="2f0ec-120">-ToJsonString</span></span>
<span data-ttu-id="2f0ec-121">Gibt an, dass die Definition als JSON-Zeichenfolge exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="2f0ec-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="2f0ec-122">-WebService</span></span>
<span data-ttu-id="2f0ec-123">Das zu exportierenden Web Service-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="2f0ec-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f0ec-124">-Confirm</span></span>
<span data-ttu-id="2f0ec-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f0ec-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f0ec-126">-WhatIf</span></span>
<span data-ttu-id="2f0ec-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f0ec-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f0ec-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f0ec-129">CommonParameters</span></span>
<span data-ttu-id="2f0ec-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f0ec-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f0ec-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f0ec-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f0ec-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f0ec-132">INPUTS</span></span>

### <span data-ttu-id="2f0ec-133">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="2f0ec-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="2f0ec-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f0ec-134">OUTPUTS</span></span>

### <span data-ttu-id="2f0ec-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2f0ec-135">System.String</span></span>

## <span data-ttu-id="2f0ec-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f0ec-136">NOTES</span></span>
<span data-ttu-id="2f0ec-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="2f0ec-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2f0ec-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f0ec-138">RELATED LINKS</span></span>
