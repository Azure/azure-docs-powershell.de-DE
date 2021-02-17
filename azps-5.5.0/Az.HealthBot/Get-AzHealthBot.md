---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: f7e1f596aef9169a1238f505d39f0dd201dcd8bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147812"
---
# <span data-ttu-id="65415-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="65415-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="65415-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65415-102">SYNOPSIS</span></span>
<span data-ttu-id="65415-103">Holen Sie sich einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="65415-103">Get a HealthBot.</span></span>

## <span data-ttu-id="65415-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65415-104">SYNTAX</span></span>

### <span data-ttu-id="65415-105">Liste1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="65415-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="65415-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="65415-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="65415-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="65415-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="65415-108">Liste</span><span class="sxs-lookup"><span data-stu-id="65415-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="65415-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="65415-109">DESCRIPTION</span></span>
<span data-ttu-id="65415-110">Holen Sie sich einen HealthBot.</span><span class="sxs-lookup"><span data-stu-id="65415-110">Get a HealthBot.</span></span>

## <span data-ttu-id="65415-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="65415-111">EXAMPLES</span></span>

### <span data-ttu-id="65415-112">Beispiel 1: Alle HealthBot erhalten</span><span class="sxs-lookup"><span data-stu-id="65415-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="65415-113">Alles von HealthBot erhalten</span><span class="sxs-lookup"><span data-stu-id="65415-113">Get all HealthBot</span></span>

### <span data-ttu-id="65415-114">Beispiel 2: "Get all HealthBot by ResourceGroupName"</span><span class="sxs-lookup"><span data-stu-id="65415-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="65415-115">Get all HealthBot by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65415-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="65415-116">Beispiel 3: Get HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="65415-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="65415-117">Get HealthBot by ResourceGroupName and Name</span><span class="sxs-lookup"><span data-stu-id="65415-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="65415-118">Beispiel 4: Get HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="65415-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="65415-119">Get HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="65415-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="65415-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65415-120">PARAMETERS</span></span>

### <span data-ttu-id="65415-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65415-121">-DefaultProfile</span></span>
<span data-ttu-id="65415-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="65415-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65415-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65415-123">-InputObject</span></span>
<span data-ttu-id="65415-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="65415-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="65415-125">-Name</span><span class="sxs-lookup"><span data-stu-id="65415-125">-Name</span></span>
<span data-ttu-id="65415-126">Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="65415-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="65415-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65415-127">-ResourceGroupName</span></span>
<span data-ttu-id="65415-128">Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="65415-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="65415-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65415-129">-SubscriptionId</span></span>
<span data-ttu-id="65415-130">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="65415-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="65415-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65415-131">CommonParameters</span></span>
<span data-ttu-id="65415-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65415-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65415-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65415-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65415-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="65415-134">INPUTS</span></span>

### <span data-ttu-id="65415-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="65415-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="65415-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="65415-136">OUTPUTS</span></span>

### <span data-ttu-id="65415-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="65415-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="65415-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="65415-138">NOTES</span></span>

<span data-ttu-id="65415-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="65415-139">ALIASES</span></span>

<span data-ttu-id="65415-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="65415-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="65415-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="65415-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="65415-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="65415-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="65415-143">INPUTOBJECT <IHealthBotIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="65415-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="65415-144">`[BotName <String>]`: Der Name der Bot-Ressource.</span><span class="sxs-lookup"><span data-stu-id="65415-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="65415-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="65415-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="65415-146">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe "Bot" im Benutzerabonnement.</span><span class="sxs-lookup"><span data-stu-id="65415-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="65415-147">`[SubscriptionId <String>]`: Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="65415-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="65415-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="65415-148">RELATED LINKS</span></span>

