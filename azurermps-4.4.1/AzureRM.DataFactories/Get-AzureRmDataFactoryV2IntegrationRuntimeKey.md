---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503242"
---
# <span data-ttu-id="0a73f-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a73f-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="0a73f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a73f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a73f-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="0a73f-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a73f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a73f-104">SYNTAX</span></span>

### <span data-ttu-id="0a73f-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a73f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a73f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0a73f-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a73f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0a73f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a73f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a73f-108">DESCRIPTION</span></span>
<span data-ttu-id="0a73f-109">Abrufen von Schlüsseln für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="0a73f-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="0a73f-110">Die Schlüssel werden zum Registrieren eines Integrationslauf Zeit Knotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="0a73f-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="0a73f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a73f-111">EXAMPLES</span></span>

### <span data-ttu-id="0a73f-112">Beispiel 1: Abrufen von Integrationslauf Zeit Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="0a73f-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="0a73f-113">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" ab.</span><span class="sxs-lookup"><span data-stu-id="0a73f-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="0a73f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a73f-114">PARAMETERS</span></span>

### <span data-ttu-id="0a73f-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0a73f-115">-DataFactoryName</span></span>
<span data-ttu-id="0a73f-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="0a73f-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73f-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a73f-117">-InputObject</span></span>
<span data-ttu-id="0a73f-118">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="0a73f-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0a73f-119">-Name</span></span>
<span data-ttu-id="0a73f-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="0a73f-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a73f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a73f-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a73f-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73f-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0a73f-123">-ResourceId</span></span>
<span data-ttu-id="0a73f-124">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0a73f-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a73f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a73f-125">-DefaultProfile</span></span>
<span data-ttu-id="0a73f-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a73f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a73f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a73f-127">CommonParameters</span></span>
<span data-ttu-id="0a73f-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a73f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a73f-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a73f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a73f-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a73f-130">INPUTS</span></span>

### <span data-ttu-id="0a73f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0a73f-131">System.String</span></span>
<span data-ttu-id="0a73f-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a73f-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="0a73f-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a73f-133">OUTPUTS</span></span>

### <span data-ttu-id="0a73f-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="0a73f-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="0a73f-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a73f-135">NOTES</span></span>

## <span data-ttu-id="0a73f-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a73f-136">RELATED LINKS</span></span>

[<span data-ttu-id="0a73f-137">Neu – AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="0a73f-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
