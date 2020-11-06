---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: 45e0fe4583477b05d4218f9e7b3ffb920b0218d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497389"
---
# <span data-ttu-id="f8a09-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f8a09-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="f8a09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8a09-102">SYNOPSIS</span></span>
<span data-ttu-id="f8a09-103">Exportiert das Web Service Definition-Objekt als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8a09-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8a09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8a09-104">SYNTAX</span></span>

### <span data-ttu-id="f8a09-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="f8a09-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8a09-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="f8a09-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8a09-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8a09-107">DESCRIPTION</span></span>
<span data-ttu-id="f8a09-108">Exportiert das Definitionsobjekt für das angegebene Web Servive als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f8a09-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="f8a09-109">Sie können die Zeichenfolge sofort zurückgeben oder in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="f8a09-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="f8a09-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8a09-110">EXAMPLES</span></span>

### <span data-ttu-id="f8a09-111">Beispiel 1: Exportieren als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f8a09-111">Example 1: Export as string</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="f8a09-112">Beispiel 2: Exportieren in eine Datei</span><span class="sxs-lookup"><span data-stu-id="f8a09-112">Example 2: Export to file</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="f8a09-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8a09-113">PARAMETERS</span></span>

### <span data-ttu-id="f8a09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8a09-114">-DefaultProfile</span></span>
<span data-ttu-id="f8a09-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f8a09-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8a09-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f8a09-116">-Force</span></span>
<span data-ttu-id="f8a09-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f8a09-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f8a09-118">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="f8a09-118">-OutputFile</span></span>
<span data-ttu-id="f8a09-119">Der Dateipfad für die exportierte Definition.</span><span class="sxs-lookup"><span data-stu-id="f8a09-119">The file path for exported definition.</span></span>

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

### <span data-ttu-id="f8a09-120">-Tojsonl</span><span class="sxs-lookup"><span data-stu-id="f8a09-120">-ToJsonString</span></span>
<span data-ttu-id="f8a09-121">Gibt an, dass die Definition als JSON-Zeichenfolge exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="f8a09-121">Specifies that the definition will be exported as a JSON string.</span></span>

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

### <span data-ttu-id="f8a09-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="f8a09-122">-WebService</span></span>
<span data-ttu-id="f8a09-123">Das zu exportierenden Web Service-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f8a09-123">The web service definition object to be exported.</span></span>

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

### <span data-ttu-id="f8a09-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8a09-124">-Confirm</span></span>
<span data-ttu-id="f8a09-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8a09-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8a09-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8a09-126">-WhatIf</span></span>
<span data-ttu-id="f8a09-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8a09-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8a09-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8a09-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8a09-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8a09-129">CommonParameters</span></span>
<span data-ttu-id="f8a09-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8a09-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8a09-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8a09-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8a09-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8a09-132">INPUTS</span></span>

### <span data-ttu-id="f8a09-133">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="f8a09-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="f8a09-134">Parameter: Webservice (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8a09-134">Parameters: WebService (ByValue)</span></span>

## <span data-ttu-id="f8a09-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8a09-135">OUTPUTS</span></span>

### <span data-ttu-id="f8a09-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f8a09-136">System.String</span></span>

## <span data-ttu-id="f8a09-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8a09-137">NOTES</span></span>
<span data-ttu-id="f8a09-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f8a09-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f8a09-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8a09-139">RELATED LINKS</span></span>
