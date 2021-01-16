---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratediscoveredserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateDiscoveredServer.md
ms.openlocfilehash: 367d22f4cea200b59b63e3ddb39c1eaad749fc43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366889"
---
# <span data-ttu-id="4216c-101">Get-AzMigrateDiscoveredServer</span><span class="sxs-lookup"><span data-stu-id="4216c-101">Get-AzMigrateDiscoveredServer</span></span>

## <span data-ttu-id="4216c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4216c-102">SYNOPSIS</span></span>
<span data-ttu-id="4216c-103">"Alle ermittelten Server in einem Migrieren-Projekt erhalten" aus.</span><span class="sxs-lookup"><span data-stu-id="4216c-103">Get All discovered servers in a migrate project.</span></span>

## <span data-ttu-id="4216c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4216c-104">SYNTAX</span></span>

### <span data-ttu-id="4216c-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4216c-105">List (Default)</span></span>
```
Get-AzMigrateDiscoveredServer -ProjectName <String> -ResourceGroupName <String> [-DisplayName <String>]
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4216c-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4216c-106">Get</span></span>
```
Get-AzMigrateDiscoveredServer -Name <String> -ProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4216c-107">GetInSite</span><span class="sxs-lookup"><span data-stu-id="4216c-107">GetInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -Name <String> -ProjectName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4216c-108">ListInSite</span><span class="sxs-lookup"><span data-stu-id="4216c-108">ListInSite</span></span>
```
Get-AzMigrateDiscoveredServer -ApplianceName <String> -ProjectName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-SubscriptionId <String[]>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4216c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4216c-109">DESCRIPTION</span></span>
<span data-ttu-id="4216c-110">Abrufen des Azure Migrate Server Commandlets ruft alle Server in einem Migrierenprojekt ab.</span><span class="sxs-lookup"><span data-stu-id="4216c-110">Get Azure migrate server commandlet fetches all servers in a migrate project.</span></span>

## <span data-ttu-id="4216c-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4216c-111">EXAMPLES</span></span>

### <span data-ttu-id="4216c-112">Beispiel 1: Liste</span><span class="sxs-lookup"><span data-stu-id="4216c-112">Example 1: List</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="4216c-113">Holen Sie sich alle Server in einem Migrieren-Projekt.</span><span class="sxs-lookup"><span data-stu-id="4216c-113">Get All servers in a migrate project.</span></span>

### <span data-ttu-id="4216c-114">Beispiel 2: Erhalten</span><span class="sxs-lookup"><span data-stu-id="4216c-114">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="4216c-115">Holen Sie sich einen Server in einem Migrierenprojekt nach Name.</span><span class="sxs-lookup"><span data-stu-id="4216c-115">Get a server in a migrate project by name.</span></span>
<span data-ttu-id="4216c-116">"Name" ist ein eindeutiger Parameter für einen Server.</span><span class="sxs-lookup"><span data-stu-id="4216c-116">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="4216c-117">Beispiel 3: Liste in einem Gerät</span><span class="sxs-lookup"><span data-stu-id="4216c-117">Example 3: List in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c180-1359-5e3c-3f56-05632aa4a37f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029d80d-d014-72f3-8d05-d43ee49a023d Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029bd24-6d40-88dc-4f29-329596f9a50b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50292d97-2025-bfdf-1f07-86afa50d144f Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50293685-fb73-0a89-204f-f79cb1f0061e Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029c9aa-3c8c-aba8-834e-1058bc457e5b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029dabc-cc94-780f-76fd-e39acb0e9dce Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_50299579-fc18-4152-ade2-c4a57946f72b Microsoft.OffAzure/VMwareSites/machines
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029cc18-efdc-7315-3b09-9d12a0f337e2 Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="4216c-118">Listen Sie alle Server für ein Gerät in einem Projekt auf.</span><span class="sxs-lookup"><span data-stu-id="4216c-118">List all servers for an appliance in a project.</span></span>

### <span data-ttu-id="4216c-119">Beispiel 4: Ein Gerät verwenden</span><span class="sxs-lookup"><span data-stu-id="4216c-119">Example 4: Get in an appliance</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer -Name idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc -ApplianceName BBVMwareAVS -SubscriptionId xxx-xxx-xxx -ResourceGroupName julytest -ProjectName julytest

Name                                                                                                      Typeo…
----                                                                                                      ----o…
idclab-a360-fareast-corp-micros-86617dcf-effe-59ad-8c3a-cdd3ea7300d3_5029e62c-31d2-a6c3-5316-aa39f47c49fc Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="4216c-120">Holen Sie sich einen Server für eine Einheit in einem Projekt.</span><span class="sxs-lookup"><span data-stu-id="4216c-120">Get a server for an appliance in a project.</span></span>
<span data-ttu-id="4216c-121">"Name" ist ein eindeutiger Parameter für einen Server.</span><span class="sxs-lookup"><span data-stu-id="4216c-121">Name is a unique paramenter for a server.</span></span>

### <span data-ttu-id="4216c-122">Beispiel 5: Auflisten und Filtern nach Anzeigename</span><span class="sxs-lookup"><span data-stu-id="4216c-122">Example 5: List and filter by display name</span></span>
```powershell
PS C:\> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines

```

<span data-ttu-id="4216c-123">ListenServer in einem Projekt migrieren und Antworten mit Anzeigenamen filtern</span><span class="sxs-lookup"><span data-stu-id="4216c-123">List servers in a migrate project and filter responses with display name.</span></span>

### <span data-ttu-id="4216c-124">Beispiel 6: Auflisten in einem Gerät und Filtern nach Anzeigename</span><span class="sxs-lookup"><span data-stu-id="4216c-124">Example 6: List in an appliance and filter by display name</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateDiscoveredServer  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -ProjectName BugBashAVSVMware -ApplianceName BBVMwareAVS -DisplayName Contoso | Format-Table DisplayName,Name,Type

DisplayName                   Name                                                                                  Type
-----------                   ----                                                                                  ----
Contoso-ConfigurationServer   10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50098b08-5701-4c58-f6ad-1daf127a8ed9 Microsoft.OffAzure/VMwareSites/machines
Contoso-FrontTier1            10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009c31a-241a-8213-5627-4ea4af00df93 Microsoft.OffAzure/VMwareSites/machines
Contoso-MiddleTier1           10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097bb8-f32c-39d6-f475-5aaa6194f016 Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv2                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_5009b455-1721-fa03-7ceb-8177cd2c5de6 Microsoft.OffAzure/VMwareSites/machines
ContosoCSASR                  10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50096b80-7061-672c-8db0-07ee41212869 Microsoft.OffAzure/VMwareSites/machines
ContosoVMwareMigration2       10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50099d31-71d5-2bd1-fada-8c4eba2f279a Microsoft.OffAzure/VMwareSites/machines
ContosoAppSrv1                10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_50097d3f-c1f6-9217-825c-936db54043df Microsoft.OffAzure/VMwareSites/machines
Contoso-DataTier3             10-150-8-52-b090bef3-b733-5e34-bc8f-eb6f2701432a_500986e5-7720-471e-11d7-d4e8ae9edc45 Microsoft.OffAzure/VMwareSites/machines
```

<span data-ttu-id="4216c-125">Listenserver für ein Gerät in einem Migrieren eines Projekts und Filtern von Antworten mit Anzeigename.</span><span class="sxs-lookup"><span data-stu-id="4216c-125">List servers for an appliance in a migrate project and filter responses with display name.</span></span>

## <span data-ttu-id="4216c-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4216c-126">PARAMETERS</span></span>

### <span data-ttu-id="4216c-127">-ApplianceName</span><span class="sxs-lookup"><span data-stu-id="4216c-127">-ApplianceName</span></span>
<span data-ttu-id="4216c-128">Gibt den Namen des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="4216c-128">Specifies the appliance name.</span></span>
<span data-ttu-id="4216c-129">Dies ist intern einer Website zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="4216c-129">This internally maps to a site.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInSite, ListInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-130">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4216c-130">-DisplayName</span></span>
<span data-ttu-id="4216c-131">Gibt den Anzeigenamen des VMware Computers an.</span><span class="sxs-lookup"><span data-stu-id="4216c-131">Specifies the VMware machine display name.</span></span>

```yaml
Type: System.String
Parameter Sets: List, ListInSite
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4216c-132">-Name</span></span>
<span data-ttu-id="4216c-133">Gibt den Namen des VMware-Computers an.</span><span class="sxs-lookup"><span data-stu-id="4216c-133">Specifies the VMware machine name.</span></span>
<span data-ttu-id="4216c-134">Dies ist ein interner Name.</span><span class="sxs-lookup"><span data-stu-id="4216c-134">This is an internal Name.</span></span>
<span data-ttu-id="4216c-135">Verwenden Sie für Benutzer den Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="4216c-135">For users, use display name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetInSite
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-136">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="4216c-136">-ProjectName</span></span>
<span data-ttu-id="4216c-137">Gibt den Namen des Projekts "Migrieren" an.</span><span class="sxs-lookup"><span data-stu-id="4216c-137">Specifies the migrate project name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4216c-138">-ResourceGroupName</span></span>
<span data-ttu-id="4216c-139">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4216c-139">Specifies the resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4216c-140">-SubscriptionId</span></span>
<span data-ttu-id="4216c-141">Gibt die Abonnement-ID an.</span><span class="sxs-lookup"><span data-stu-id="4216c-141">Specifies the subscription id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4216c-142">-Confirm</span></span>
<span data-ttu-id="4216c-143">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4216c-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-144">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4216c-144">-WhatIf</span></span>
<span data-ttu-id="4216c-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4216c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4216c-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4216c-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4216c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4216c-147">CommonParameters</span></span>
<span data-ttu-id="4216c-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4216c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4216c-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4216c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4216c-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4216c-150">INPUTS</span></span>

## <span data-ttu-id="4216c-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4216c-151">OUTPUTS</span></span>

### <span data-ttu-id="4216c-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span><span class="sxs-lookup"><span data-stu-id="4216c-152">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareMachine</span></span>

## <span data-ttu-id="4216c-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4216c-153">NOTES</span></span>

<span data-ttu-id="4216c-154">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4216c-154">ALIASES</span></span>

## <span data-ttu-id="4216c-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4216c-155">RELATED LINKS</span></span>

