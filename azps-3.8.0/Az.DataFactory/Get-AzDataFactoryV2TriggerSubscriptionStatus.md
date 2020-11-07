---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2triggersubscriptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2TriggerSubscriptionStatus.md
ms.openlocfilehash: 62418f0840e2bbeef016d53c3136f155c4de055f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847264"
---
# <span data-ttu-id="a5184-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a5184-101">Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>

## <span data-ttu-id="a5184-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5184-102">SYNOPSIS</span></span>
<span data-ttu-id="a5184-103">Abrufen des Status des Abonnements für den Ereignisauslöser für die angegebenen externen Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="a5184-103">Get the status of the subscription for the event trigger to the specified external service events.</span></span>

## <span data-ttu-id="a5184-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5184-104">SYNTAX</span></span>

### <span data-ttu-id="a5184-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5184-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5184-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5184-106">ByInputObject</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-InputObject] <PSTrigger>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a5184-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a5184-107">ByResourceId</span></span>
```
Get-AzDataFactoryV2TriggerSubscriptionStatus [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5184-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5184-108">DESCRIPTION</span></span>
<span data-ttu-id="a5184-109">Dieser Befehl ruft den Status des Abonnements für den Ereignisauslöser für die angegebenen externen Dienstereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="a5184-109">This command gets the status of the subscription for the event trigger to the specified external service events.</span></span> <span data-ttu-id="a5184-110">Der Trigger kann erst gestartet werden, wenn der zurückgegebene Status "aktiviert" ist.</span><span class="sxs-lookup"><span data-stu-id="a5184-110">The trigger can't be started until the returned status is "Enabled".</span></span>

## <span data-ttu-id="a5184-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5184-111">EXAMPLES</span></span>

### <span data-ttu-id="a5184-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5184-112">Example 1</span></span>
```
PS C:\> Get-AzDataFactoryV2TriggerSubscriptionStatus -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Enabled
```

<span data-ttu-id="a5184-113">Mit diesem Befehl wird der Status des Kontroll for BlobEnetTrigger1-Triggers für die externen Dienstereignisse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a5184-113">This command will get the status of the subscribtion for BlobEnetTrigger1 trigger to the external service events.</span></span>

## <span data-ttu-id="a5184-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5184-114">PARAMETERS</span></span>

### <span data-ttu-id="a5184-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a5184-115">-DataFactoryName</span></span>
<span data-ttu-id="a5184-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a5184-116">The data factory name.</span></span>

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

### <span data-ttu-id="a5184-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5184-117">-DefaultProfile</span></span>
<span data-ttu-id="a5184-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5184-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5184-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5184-119">-InputObject</span></span>
<span data-ttu-id="a5184-120">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a5184-120">The trigger object.</span></span>

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

### <span data-ttu-id="a5184-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a5184-121">-Name</span></span>
<span data-ttu-id="a5184-122">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="a5184-122">The trigger name.</span></span>

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

### <span data-ttu-id="a5184-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5184-123">-ResourceGroupName</span></span>
<span data-ttu-id="a5184-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a5184-124">The resource group name.</span></span>

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

### <span data-ttu-id="a5184-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a5184-125">-ResourceId</span></span>
<span data-ttu-id="a5184-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a5184-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a5184-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5184-127">CommonParameters</span></span>
<span data-ttu-id="a5184-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5184-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5184-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5184-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5184-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5184-130">INPUTS</span></span>

### <span data-ttu-id="a5184-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a5184-131">System.String</span></span>
<span data-ttu-id="a5184-132">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a5184-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="a5184-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5184-133">OUTPUTS</span></span>

### <span data-ttu-id="a5184-134">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a5184-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="a5184-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5184-135">NOTES</span></span>

## <span data-ttu-id="a5184-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5184-136">RELATED LINKS</span></span>

