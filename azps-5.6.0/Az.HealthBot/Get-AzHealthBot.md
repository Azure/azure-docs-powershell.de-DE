---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949232"
---
# <span data-ttu-id="6643d-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="6643d-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="6643d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6643d-102">SYNOPSIS</span></span>
<span data-ttu-id="6643d-103">Holen Sie sich einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="6643d-103">Get a HealthBot.</span></span>

## <span data-ttu-id="6643d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6643d-104">SYNTAX</span></span>

### <span data-ttu-id="6643d-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="6643d-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6643d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6643d-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6643d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6643d-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6643d-108">Liste</span><span class="sxs-lookup"><span data-stu-id="6643d-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6643d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6643d-109">DESCRIPTION</span></span>
<span data-ttu-id="6643d-110">Holen Sie sich einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="6643d-110">Get a HealthBot.</span></span>

## <span data-ttu-id="6643d-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6643d-111">EXAMPLES</span></span>

### <span data-ttu-id="6643d-112">Beispiel 1: Alle HealthBot herunterladen</span><span class="sxs-lookup"><span data-stu-id="6643d-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="6643d-113">Alle HealthBot herunterladen</span><span class="sxs-lookup"><span data-stu-id="6643d-113">Get all HealthBot</span></span>

### <span data-ttu-id="6643d-114">Beispiel 2: Alle HealthBot nach ResourceGroupName herunterladen</span><span class="sxs-lookup"><span data-stu-id="6643d-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="6643d-115">Alle HealthBot nach ResourceGroupName herunterladen</span><span class="sxs-lookup"><span data-stu-id="6643d-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="6643d-116">Beispiel 3: Get HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="6643d-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="6643d-117">HealthBot nach ResourceGroupName und Name herunterladen</span><span class="sxs-lookup"><span data-stu-id="6643d-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="6643d-118">Beispiel 4: Get HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="6643d-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="6643d-119">Get HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="6643d-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="6643d-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6643d-120">PARAMETERS</span></span>

### <span data-ttu-id="6643d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6643d-121">-DefaultProfile</span></span>
<span data-ttu-id="6643d-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6643d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6643d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6643d-123">-InputObject</span></span>
<span data-ttu-id="6643d-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="6643d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6643d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6643d-125">-Name</span></span>
<span data-ttu-id="6643d-126">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6643d-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6643d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6643d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6643d-128">Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="6643d-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6643d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6643d-129">-SubscriptionId</span></span>
<span data-ttu-id="6643d-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6643d-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6643d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6643d-131">CommonParameters</span></span>
<span data-ttu-id="6643d-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6643d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6643d-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6643d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6643d-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6643d-134">INPUTS</span></span>

### <span data-ttu-id="6643d-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="6643d-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="6643d-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6643d-136">OUTPUTS</span></span>

### <span data-ttu-id="6643d-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="6643d-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="6643d-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6643d-138">NOTES</span></span>

<span data-ttu-id="6643d-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6643d-139">ALIASES</span></span>

<span data-ttu-id="6643d-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="6643d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6643d-141">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="6643d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6643d-142">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6643d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6643d-143">INPUTOBJECT <IHealthBotIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="6643d-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6643d-144">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="6643d-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="6643d-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="6643d-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6643d-146">`[ResourceGroupName <String>]`: Der Name der Bot-Ressourcengruppe im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="6643d-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="6643d-147">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="6643d-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="6643d-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6643d-148">RELATED LINKS</span></span>

