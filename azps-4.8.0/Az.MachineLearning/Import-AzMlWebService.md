---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010166"
---
# <span data-ttu-id="ae414-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ae414-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="ae414-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae414-102">SYNOPSIS</span></span>
<span data-ttu-id="ae414-103">Importiert ein JSON-Objekt in eine Web Service-Definition.</span><span class="sxs-lookup"><span data-stu-id="ae414-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="ae414-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae414-104">SYNTAX</span></span>

### <span data-ttu-id="ae414-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="ae414-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae414-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="ae414-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae414-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae414-107">DESCRIPTION</span></span>
<span data-ttu-id="ae414-108">Das Import-AzMlWebService-Cmdlet importiert, entweder direkt oder in einer referenzierten Datei, und erstellt ein Webdienst-Definitionsobjekt, das an das New-AzMlWebService-Cmdlet übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae414-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="ae414-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae414-109">EXAMPLES</span></span>

### <span data-ttu-id="ae414-110">Beispiel 1: Importieren aus einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ae414-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="ae414-111">Beispiel 2: Importieren aus Dateipfad</span><span class="sxs-lookup"><span data-stu-id="ae414-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="ae414-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae414-112">PARAMETERS</span></span>

### <span data-ttu-id="ae414-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae414-113">-DefaultProfile</span></span>
<span data-ttu-id="ae414-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ae414-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae414-115">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="ae414-115">-InputFile</span></span>
<span data-ttu-id="ae414-116">Der Pfad zu der Datei, die die zu importierende Web Service-Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="ae414-116">The path to the file containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae414-117">-JSON.</span><span class="sxs-lookup"><span data-stu-id="ae414-117">-JsonString</span></span>
<span data-ttu-id="ae414-118">Die JSON-formatierte Zeichenfolge, die die zu importierende Webdienstdefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="ae414-118">The JSON formatted string containing the web service definition to import.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromJSONString.
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae414-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae414-119">CommonParameters</span></span>
<span data-ttu-id="ae414-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae414-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae414-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae414-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae414-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae414-122">INPUTS</span></span>

### <span data-ttu-id="ae414-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ae414-123">None</span></span>

## <span data-ttu-id="ae414-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae414-124">OUTPUTS</span></span>

### <span data-ttu-id="ae414-125">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ae414-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ae414-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae414-126">NOTES</span></span>
<span data-ttu-id="ae414-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ae414-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ae414-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae414-128">RELATED LINKS</span></span>
