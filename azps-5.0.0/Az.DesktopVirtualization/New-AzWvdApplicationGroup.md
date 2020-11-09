---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplicationGroup.md
ms.openlocfilehash: 0dfbcabcb1869457e29d6c16c861c0743f50dc5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297045"
---
# <span data-ttu-id="5d16a-101">New-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5d16a-101">New-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="5d16a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d16a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d16a-103">Erstellen oder aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-103">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="5d16a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d16a-104">SYNTAX</span></span>

```
New-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String>
 -ApplicationGroupType <ApplicationGroupType> -HostPoolArmPath <String> -Location <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d16a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d16a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d16a-106">Erstellen oder aktualisieren Sie eine ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-106">Create or update an applicationGroup.</span></span>

## <span data-ttu-id="5d16a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d16a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d16a-108">Beispiel 1: Erstellen einer virtuellen Windows-Desktop Anwendung mit Namen</span><span class="sxs-lookup"><span data-stu-id="5d16a-108">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'RemoteApp'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5d16a-109">Mit diesem Befehl wird eine Windows Virtual Desktop-Anwendungsgruppe in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d16a-109">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

### <span data-ttu-id="5d16a-110">Beispiel 2: Erstellen einer Windows-virtuellen Desktop Anwendung mit Namen</span><span class="sxs-lookup"><span data-stu-id="5d16a-110">Example 2: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -Location 'eastus' `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `
                            -HostPoolArmPath '/subscriptions/SubscriptionId/resourcegroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/hostPools/HostPoolName' `
                            -ApplicationGroupType 'Desktop'

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="5d16a-111">Mit diesem Befehl wird eine Windows Virtual Desktop-Anwendungsgruppe in einer Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="5d16a-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="5d16a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d16a-112">PARAMETERS</span></span>

### <span data-ttu-id="5d16a-113">-ApplicationGroupType</span><span class="sxs-lookup"><span data-stu-id="5d16a-113">-ApplicationGroupType</span></span>
<span data-ttu-id="5d16a-114">Der Ressourcentyp von ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-114">Resource Type of ApplicationGroup.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.ApplicationGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d16a-115">-DefaultProfile</span></span>
<span data-ttu-id="5d16a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d16a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d16a-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d16a-117">-Description</span></span>
<span data-ttu-id="5d16a-118">Beschreibung von ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-118">Description of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="5d16a-119">-FriendlyName</span></span>
<span data-ttu-id="5d16a-120">Anzeigename der ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-120">Friendly name of ApplicationGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-121">-HostPoolArmPath</span><span class="sxs-lookup"><span data-stu-id="5d16a-121">-HostPoolArmPath</span></span>
<span data-ttu-id="5d16a-122">HostPool Path von ApplicationGroup.</span><span class="sxs-lookup"><span data-stu-id="5d16a-122">HostPool arm path of ApplicationGroup.</span></span>

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

### <span data-ttu-id="5d16a-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="5d16a-123">-Location</span></span>
<span data-ttu-id="5d16a-124">Der Geo-Standort, an dem die Ressource wohnt</span><span class="sxs-lookup"><span data-stu-id="5d16a-124">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="5d16a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5d16a-125">-Name</span></span>
<span data-ttu-id="5d16a-126">Der Name der Anwendungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5d16a-126">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d16a-127">-ResourceGroupName</span></span>
<span data-ttu-id="5d16a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d16a-128">The name of the resource group.</span></span>
<span data-ttu-id="5d16a-129">Bei dem Namen wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="5d16a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5d16a-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5d16a-130">-SubscriptionId</span></span>
<span data-ttu-id="5d16a-131">Die ID des zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5d16a-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d16a-132">-Tag</span></span>
<span data-ttu-id="5d16a-133">Ressourcenkategorien.</span><span class="sxs-lookup"><span data-stu-id="5d16a-133">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d16a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d16a-134">-Confirm</span></span>
<span data-ttu-id="5d16a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d16a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d16a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d16a-136">-WhatIf</span></span>
<span data-ttu-id="5d16a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d16a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d16a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d16a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d16a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d16a-139">CommonParameters</span></span>
<span data-ttu-id="5d16a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d16a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d16a-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d16a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d16a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d16a-142">INPUTS</span></span>

## <span data-ttu-id="5d16a-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d16a-143">OUTPUTS</span></span>

### <span data-ttu-id="5d16a-144">Microsoft. Azure. PowerShell. Cmdlets. DesktopVirtualization. Models. Api20191210Preview. IApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="5d16a-144">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="5d16a-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d16a-145">NOTES</span></span>

<span data-ttu-id="5d16a-146">Aliase</span><span class="sxs-lookup"><span data-stu-id="5d16a-146">ALIASES</span></span>

## <span data-ttu-id="5d16a-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d16a-147">RELATED LINKS</span></span>

