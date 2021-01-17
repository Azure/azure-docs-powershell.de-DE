---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/import-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Import-AzMlWebService.md
ms.openlocfilehash: 90416cd786e13bdd0232aebfcff2cd6963c1f872
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360771"
---
# <span data-ttu-id="ed371-101">Import-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="ed371-101">Import-AzMlWebService</span></span>

## <span data-ttu-id="ed371-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed371-102">SYNOPSIS</span></span>
<span data-ttu-id="ed371-103">Importiert ein JSON-Objekt in eine Webdienstdefinition.</span><span class="sxs-lookup"><span data-stu-id="ed371-103">Imports a JSON object into a web service definition.</span></span>

## <span data-ttu-id="ed371-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed371-104">SYNTAX</span></span>

### <span data-ttu-id="ed371-105">ImportFromJSONFile</span><span class="sxs-lookup"><span data-stu-id="ed371-105">ImportFromJSONFile</span></span>
```
Import-AzMlWebService -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed371-106">ImportFromJSONString.</span><span class="sxs-lookup"><span data-stu-id="ed371-106">ImportFromJSONString.</span></span>
```
Import-AzMlWebService -JsonString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed371-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed371-107">DESCRIPTION</span></span>
<span data-ttu-id="ed371-108">Das Import-AzMlWebService importiert , wird entweder direkt oder in einer Referenzdatei angegeben und erstellt ein Webdienstdefinitionsobjekt, das an das cmdlet New-AzMlWebService übergeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ed371-108">The Import-AzMlWebService cmdlet imports , specified either directly or in a referenced file, and creates a web service definition object that can be passed to the New-AzMlWebService cmdlet.</span></span>

## <span data-ttu-id="ed371-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed371-109">EXAMPLES</span></span>

### <span data-ttu-id="ed371-110">Beispiel 1: Importieren aus einer Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ed371-110">Example 1: Import from string</span></span>
```
Import-AzMlWebService -JsonString $jsonDefinition
```

### <span data-ttu-id="ed371-111">Beispiel 2: Importieren aus dateipfad</span><span class="sxs-lookup"><span data-stu-id="ed371-111">Example 2: Import from file path</span></span>
```
Import-AzMlWebService -InputFile "C:\mlservice.json"
```

## <span data-ttu-id="ed371-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed371-112">PARAMETERS</span></span>

### <span data-ttu-id="ed371-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed371-113">-DefaultProfile</span></span>
<span data-ttu-id="ed371-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ed371-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed371-115">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ed371-115">-InputFile</span></span>
<span data-ttu-id="ed371-116">Der Pfad zu der Datei, die die zu importierende Webdienstdefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="ed371-116">The path to the file containing the web service definition to import.</span></span>

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

### <span data-ttu-id="ed371-117">-JsonString</span><span class="sxs-lookup"><span data-stu-id="ed371-117">-JsonString</span></span>
<span data-ttu-id="ed371-118">Die formatierte JSON-Zeichenfolge, die die zu importierende Webdienstdefinition enthält.</span><span class="sxs-lookup"><span data-stu-id="ed371-118">The JSON formatted string containing the web service definition to import.</span></span>

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

### <span data-ttu-id="ed371-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed371-119">CommonParameters</span></span>
<span data-ttu-id="ed371-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed371-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed371-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed371-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed371-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed371-122">INPUTS</span></span>

### <span data-ttu-id="ed371-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ed371-123">None</span></span>

## <span data-ttu-id="ed371-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed371-124">OUTPUTS</span></span>

### <span data-ttu-id="ed371-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="ed371-125">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="ed371-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ed371-126">NOTES</span></span>
<span data-ttu-id="ed371-127">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span><span class="sxs-lookup"><span data-stu-id="ed371-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ed371-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ed371-128">RELATED LINKS</span></span>
