---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 2a1aaef2532e8c0a00a04a42d857e2be0e2a0451
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820416"
---
# <span data-ttu-id="03b7c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="03b7c-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="03b7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="03b7c-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="03b7c-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="03b7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03b7c-104">SYNTAX</span></span>

### <span data-ttu-id="03b7c-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="03b7c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03b7c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="03b7c-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03b7c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="03b7c-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03b7c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03b7c-108">DESCRIPTION</span></span>
<span data-ttu-id="03b7c-109">Abrufen von Schlüsseln für eine Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="03b7c-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="03b7c-110">Die Schlüssel werden zum Registrieren eines Integrationslauf Zeit Knotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="03b7c-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="03b7c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03b7c-111">EXAMPLES</span></span>

### <span data-ttu-id="03b7c-112">Beispiel 1: Abrufen von Integrationslauf Zeit Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="03b7c-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="03b7c-113">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" ab.</span><span class="sxs-lookup"><span data-stu-id="03b7c-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="03b7c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="03b7c-114">PARAMETERS</span></span>

### <span data-ttu-id="03b7c-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="03b7c-115">-DataFactoryName</span></span>
<span data-ttu-id="03b7c-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="03b7c-116">The data factory name.</span></span>

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

### <span data-ttu-id="03b7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03b7c-117">-DefaultProfile</span></span>
<span data-ttu-id="03b7c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03b7c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03b7c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03b7c-119">-InputObject</span></span>
<span data-ttu-id="03b7c-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="03b7c-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="03b7c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="03b7c-121">-Name</span></span>
<span data-ttu-id="03b7c-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="03b7c-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="03b7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03b7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="03b7c-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="03b7c-124">The resource group name.</span></span>

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

### <span data-ttu-id="03b7c-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03b7c-125">-ResourceId</span></span>
<span data-ttu-id="03b7c-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="03b7c-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="03b7c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03b7c-127">CommonParameters</span></span>
<span data-ttu-id="03b7c-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03b7c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03b7c-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03b7c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03b7c-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03b7c-130">INPUTS</span></span>

### <span data-ttu-id="03b7c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="03b7c-131">System.String</span></span>

### <span data-ttu-id="03b7c-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="03b7c-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="03b7c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03b7c-133">OUTPUTS</span></span>

### <span data-ttu-id="03b7c-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="03b7c-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="03b7c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="03b7c-135">NOTES</span></span>

## <span data-ttu-id="03b7c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03b7c-136">RELATED LINKS</span></span>

[<span data-ttu-id="03b7c-137">Neu – AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="03b7c-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
