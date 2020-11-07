---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 7c885da5423e765cca3d18ce18957c0e64bb2c36
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650675"
---
# <span data-ttu-id="ccadb-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ccadb-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="ccadb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccadb-102">SYNOPSIS</span></span>
<span data-ttu-id="ccadb-103">Importiert ein JSON-Objekt in eine Web Service-Definition.</span><span class="sxs-lookup"><span data-stu-id="ccadb-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="ccadb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccadb-104">SYNTAX</span></span>

### <span data-ttu-id="ccadb-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="ccadb-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccadb-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="ccadb-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccadb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccadb-107">DESCRIPTION</span></span>
<span data-ttu-id="ccadb-108">Das Import-AzMlWebService-Cmdlet importiert, entweder direkt oder in einer referenzierten Datei, und erstellt ein Webdienst-Definitionsobjekt, das an das New-AzMlWebService-Cmdlet übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ccadb-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="ccadb-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccadb-109">EXAMPLES</span></span>

### <span data-ttu-id="ccadb-110">Beispiel 1: Importieren aus einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ccadb-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="ccadb-111">Beispiel 2: Importieren aus Dateipfad</span><span class="sxs-lookup"><span data-stu-id="ccadb-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="ccadb-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccadb-112">PARAMETERS</span></span>

### <span data-ttu-id="ccadb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccadb-113">-DefaultProfile</span></span>
<span data-ttu-id="ccadb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ccadb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccadb-115">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="ccadb-115">-InputFile</span></span>
<span data-ttu-id="ccadb-116">Der Pfad zu der Datei, die die zu importierende Web Service-Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="ccadb-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="ccadb-117">-JSON.</span><span class="sxs-lookup"><span data-stu-id="ccadb-117">-JsonString</span></span>
<span data-ttu-id="ccadb-118">Die JSON-formatierte Zeichenfolge, die die zu importierende Webdienstdefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="ccadb-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="ccadb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccadb-119">CommonParameters</span></span>
<span data-ttu-id="ccadb-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccadb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccadb-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccadb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccadb-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccadb-122">INPUTS</span></span>

### <span data-ttu-id="ccadb-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ccadb-123">None</span></span>

## <span data-ttu-id="ccadb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccadb-124">OUTPUTS</span></span>

### <span data-ttu-id="ccadb-125">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="ccadb-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ccadb-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccadb-126">NOTES</span></span>
<span data-ttu-id="ccadb-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ccadb-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ccadb-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccadb-128">RELATED LINKS</span></span>
