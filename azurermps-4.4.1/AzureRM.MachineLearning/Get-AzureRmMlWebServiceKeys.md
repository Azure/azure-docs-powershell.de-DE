---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504902"
---
# <span data-ttu-id="1f262-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="1f262-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="1f262-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f262-102">SYNOPSIS</span></span>
<span data-ttu-id="1f262-103">Ruft die Schlüssel des Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="1f262-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f262-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f262-104">SYNTAX</span></span>

### <span data-ttu-id="1f262-105">Rufen Sie die Zugriffstasten eines Azure ml-Webdiensts mit dem Namen und der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="1f262-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f262-106">Rufen Sie die Access-KESY für die angegebene Webdienst Instanz ab.</span><span class="sxs-lookup"><span data-stu-id="1f262-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f262-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f262-107">DESCRIPTION</span></span>
<span data-ttu-id="1f262-108">Ruft die Zugriffstasten für die Runtime-APIs des Azure Machine Learning-Webdiensts ab.</span><span class="sxs-lookup"><span data-stu-id="1f262-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="1f262-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f262-109">EXAMPLES</span></span>

### <span data-ttu-id="1f262-110">--------------------------Beispiel 1: Abrufen der Schlüssel für einen Webdienst, der durch die Ressourcengruppe und den Namen angegeben wird--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f262-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="1f262-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1f262-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="1f262-112">--------------------------Beispiel 2: Abrufen von Schlüsseln für Webdienst Instanzen--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f262-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="1f262-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="1f262-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="1f262-114">$mlService ist ein Objekt vom Typ Microsoft. Azure. Management. MachineLearning. Webservices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="1f262-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="1f262-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f262-115">PARAMETERS</span></span>

### <span data-ttu-id="1f262-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="1f262-116">-MlWebService</span></span>
<span data-ttu-id="1f262-117">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1f262-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f262-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1f262-118">-Name</span></span>
<span data-ttu-id="1f262-119">Der Name des Webdiensts, für den die Zugriffstasten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1f262-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f262-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f262-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f262-121">Die Ressourcengruppe für den Webdienst.</span><span class="sxs-lookup"><span data-stu-id="1f262-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f262-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f262-122">-DefaultProfile</span></span>
<span data-ttu-id="1f262-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f262-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f262-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f262-124">CommonParameters</span></span>
<span data-ttu-id="1f262-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f262-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f262-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f262-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f262-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f262-127">INPUTS</span></span>

### <span data-ttu-id="1f262-128">Webservice</span><span class="sxs-lookup"><span data-stu-id="1f262-128">WebService</span></span>
<span data-ttu-id="1f262-129">Der Parameter "MlWebService" akzeptiert den Wert vom Typ "Webservice" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f262-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="1f262-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f262-130">OUTPUTS</span></span>

### <span data-ttu-id="1f262-131">Keine</span><span class="sxs-lookup"><span data-stu-id="1f262-131">None</span></span>

## <span data-ttu-id="1f262-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f262-132">NOTES</span></span>
<span data-ttu-id="1f262-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Machine, Machine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="1f262-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="1f262-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f262-134">RELATED LINKS</span></span>

