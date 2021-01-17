---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472669"
---
# <span data-ttu-id="9d0e4-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9d0e4-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="9d0e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d0e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0e4-103">Den Status des Abonnements für den Ereignistrigger für die angegebenen Externen Dienstereignisse erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="9d0e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d0e4-104">SYNTAX</span></span>

### <span data-ttu-id="9d0e4-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d0e4-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d0e4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d0e4-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d0e4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0e4-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d0e4-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d0e4-108">DESCRIPTION</span></span>
<span data-ttu-id="9d0e4-109">Dieser Befehl ruft den Status des Abonnements für den Ereignistrigger für die angegebenen Externen Dienstereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="9d0e4-110">Der Trigger kann erst gestartet werden, wenn der zurückgegebene Status "Aktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="9d0e4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d0e4-111">EXAMPLES</span></span>

### <span data-ttu-id="9d0e4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d0e4-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="9d0e4-113">Mit diesem Befehl wird der Status des BlobEnetTrigger1-Triggers für die externen Dienstereignisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="9d0e4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d0e4-114">PARAMETERS</span></span>

### <span data-ttu-id="9d0e4-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d0e4-115">-DataFactoryName</span></span>
<span data-ttu-id="9d0e4-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0e4-117">-DefaultProfile</span></span>
<span data-ttu-id="9d0e4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d0e4-119">-InputObject</span></span>
<span data-ttu-id="9d0e4-120">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-120">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9d0e4-121">-Name</span></span>
<span data-ttu-id="9d0e4-122">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-122">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0e4-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d0e4-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0e4-125">-ResourceId</span></span>
<span data-ttu-id="9d0e4-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d0e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0e4-127">CommonParameters</span></span>
<span data-ttu-id="9d0e4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0e4-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0e4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0e4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d0e4-130">INPUTS</span></span>

### <span data-ttu-id="9d0e4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="9d0e4-131">System.String</span></span>
<span data-ttu-id="9d0e4-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="9d0e4-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="9d0e4-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d0e4-133">OUTPUTS</span></span>

### <span data-ttu-id="9d0e4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="9d0e4-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="9d0e4-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d0e4-135">NOTES</span></span>

## <span data-ttu-id="9d0e4-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d0e4-136">RELATED LINKS</span></span>

