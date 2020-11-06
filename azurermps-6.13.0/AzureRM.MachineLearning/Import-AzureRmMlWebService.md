---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/import-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Import-AzureRmMlWebService.md
ms.openlocfilehash: b54e7cf5af7eadd0ea56687a336175650b55daa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496001"
---
# <span data-ttu-id="0d41a-101">Import-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="0d41a-101">Import-AzureRmMlWebService</span></span>

## <span data-ttu-id="0d41a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d41a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d41a-103">Importiert ein JSON-Objekt in eine Web Service-Definition.</span><span class="sxs-lookup"><span data-stu-id="0d41a-103">Imports a JSON object into a web service definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d41a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d41a-104">SYNTAX</span></span>

### <span data-ttu-id="0d41a-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="0d41a-105">ImportFromJSONFile</span></span>
```
Import-AzureRmMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d41a-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="0d41a-106">ImportFromJSONString.</span></span>
```
Import-AzureRmMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d41a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d41a-107">DESCRIPTION</span></span>
<span data-ttu-id="0d41a-108">Das Import-AzureRmMlWebService-Cmdlet importiert, entweder direkt oder in einer referenzierten Datei, und erstellt ein Webdienst-Definitionsobjekt, das an das New-AzureRmMlWebService-Cmdlet übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d41a-108">The Import-AzureRmMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzureRmMlWebService cmdlet.</span></span>

## <span data-ttu-id="0d41a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d41a-109">EXAMPLES</span></span>

### <span data-ttu-id="0d41a-110">Beispiel 1: Importieren aus einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0d41a-110">Example 1: Import from string</span></span>
```
Import-AzureRmMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="0d41a-111">Beispiel 2: Importieren aus Dateipfad</span><span class="sxs-lookup"><span data-stu-id="0d41a-111">Example 2: Import from file path</span></span>
```
Import-AzureRmMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="0d41a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d41a-112">PARAMETERS</span></span>

### <span data-ttu-id="0d41a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d41a-113">-DefaultProfile</span></span>
<span data-ttu-id="0d41a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0d41a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d41a-115">-Eingabefeld</span><span class="sxs-lookup"><span data-stu-id="0d41a-115">-InputFile</span></span>
<span data-ttu-id="0d41a-116">Der Pfad zu der Datei, die die zu importierende Web Service-Definition enthält.</span><span class="sxs-lookup"><span data-stu-id="0d41a-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="0d41a-117">-JSON.</span><span class="sxs-lookup"><span data-stu-id="0d41a-117">-JsonString</span></span>
<span data-ttu-id="0d41a-118">Die JSON-formatierte Zeichenfolge, die die zu importierende Webdienstdefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="0d41a-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="0d41a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d41a-119">CommonParameters</span></span>
<span data-ttu-id="0d41a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d41a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d41a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d41a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d41a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d41a-122">INPUTS</span></span>

### <span data-ttu-id="0d41a-123">Keine</span><span class="sxs-lookup"><span data-stu-id="0d41a-123">None</span></span>

## <span data-ttu-id="0d41a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d41a-124">OUTPUTS</span></span>

### <span data-ttu-id="0d41a-125">Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="0d41a-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0d41a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d41a-126">NOTES</span></span>
<span data-ttu-id="0d41a-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="0d41a-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0d41a-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d41a-128">RELATED LINKS</span></span>
