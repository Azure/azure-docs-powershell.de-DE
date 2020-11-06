---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/export-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Export-AzureRmMlWebService.md
ms.openlocfilehash: fd07ab55fad93fdf48df52e15db846630ba6c1f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503741"
---
# <span data-ttu-id="252f2-101">Export-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="252f2-101">Export-AzureRmMlWebService</span></span>

## <span data-ttu-id="252f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="252f2-102">SYNOPSIS</span></span>
<span data-ttu-id="252f2-103">Exportiert das Web Service Definition-Objekt als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="252f2-103">Exports the web service definition object as a JSON formatted string.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="252f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="252f2-104">SYNTAX</span></span>

### <span data-ttu-id="252f2-105">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="252f2-105">ExportToFile</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> -OutputFile <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="252f2-106">ExportToJSON</span><span class="sxs-lookup"><span data-stu-id="252f2-106">ExportToJSON</span></span>
```
Export-AzureRmMlWebService -WebService <WebService> [-ToJsonString] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252f2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="252f2-107">DESCRIPTION</span></span>
<span data-ttu-id="252f2-108">Exportiert das Definitionsobjekt für das angegebene Web Servive als JSON-formatierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="252f2-108">Exports the definition object for the specified web servive as a JSON formatted string.</span></span>
<span data-ttu-id="252f2-109">Sie können die Zeichenfolge sofort zurückgeben oder in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="252f2-109">You can return the string immediately or save it to a file.</span></span>

## <span data-ttu-id="252f2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="252f2-110">EXAMPLES</span></span>

### <span data-ttu-id="252f2-111">--------------------------Beispiel 1: Exportieren als Zeichenfolge--------------------------</span><span class="sxs-lookup"><span data-stu-id="252f2-111">--------------------------  Example 1: Export as string  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -ToJsonString
```

### <span data-ttu-id="252f2-112">--------------------------Beispiel 2: Exportieren in eine Datei--------------------------</span><span class="sxs-lookup"><span data-stu-id="252f2-112">--------------------------  Example 2: Export to file  --------------------------</span></span>
```
Export-AzureRmMlWebService -WebService $svc -OutputFile "C:\mlservice.json"
```

## <span data-ttu-id="252f2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="252f2-113">PARAMETERS</span></span>

### <span data-ttu-id="252f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252f2-114">-DefaultProfile</span></span>
<span data-ttu-id="252f2-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="252f2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="252f2-116">-Force</span></span>
<span data-ttu-id="252f2-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="252f2-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-118">-Outputdatei</span><span class="sxs-lookup"><span data-stu-id="252f2-118">-OutputFile</span></span>
<span data-ttu-id="252f2-119">Der Dateipfad für die exportierte Definition.</span><span class="sxs-lookup"><span data-stu-id="252f2-119">The file path for exported definition.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-120">-Tojsonl</span><span class="sxs-lookup"><span data-stu-id="252f2-120">-ToJsonString</span></span>
<span data-ttu-id="252f2-121">Gibt an, dass die Definition als JSON-Zeichenfolge exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="252f2-121">Specifies that the definition will be exported as a JSON string.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToJSON
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-122">-Webservice</span><span class="sxs-lookup"><span data-stu-id="252f2-122">-WebService</span></span>
<span data-ttu-id="252f2-123">Das zu exportierenden Web Service-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="252f2-123">The web service definition object to be exported.</span></span>

```yaml
Type: WebService
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="252f2-124">-Confirm</span></span>
<span data-ttu-id="252f2-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="252f2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252f2-126">-WhatIf</span></span>
<span data-ttu-id="252f2-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="252f2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252f2-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="252f2-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="252f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252f2-129">CommonParameters</span></span>
<span data-ttu-id="252f2-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252f2-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="252f2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252f2-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="252f2-132">INPUTS</span></span>

### <span data-ttu-id="252f2-133">Webservice</span><span class="sxs-lookup"><span data-stu-id="252f2-133">WebService</span></span>
<span data-ttu-id="252f2-134">Der Parameter "Webservice" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="252f2-134">Parameter 'WebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="252f2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="252f2-135">OUTPUTS</span></span>

### <span data-ttu-id="252f2-136">Keine</span><span class="sxs-lookup"><span data-stu-id="252f2-136">None</span></span>

## <span data-ttu-id="252f2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="252f2-137">NOTES</span></span>
<span data-ttu-id="252f2-138">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="252f2-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="252f2-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="252f2-139">RELATED LINKS</span></span>

