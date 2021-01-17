---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: 58ae996e4d2723d4b38b548dd8225a2a483ce8f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473073"
---
# <span data-ttu-id="a987d-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="a987d-101">New-AzHost</span></span>

## <span data-ttu-id="a987d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a987d-102">SYNOPSIS</span></span>
<span data-ttu-id="a987d-103">Erstellt einen Host.</span><span class="sxs-lookup"><span data-stu-id="a987d-103">Creates a  host.</span></span>

## <span data-ttu-id="a987d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a987d-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a987d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a987d-105">DESCRIPTION</span></span>
<span data-ttu-id="a987d-106">Mit diesem Cmdlet wird ein Host erstellt.</span><span class="sxs-lookup"><span data-stu-id="a987d-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="a987d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a987d-107">EXAMPLES</span></span>

### <span data-ttu-id="a987d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a987d-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="a987d-109">Mit diesem Befehl wird ein Host der angegebenen SKU in der angegebenen Hostgruppe und dem angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="a987d-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="a987d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a987d-110">PARAMETERS</span></span>

### <span data-ttu-id="a987d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a987d-111">-AsJob</span></span>
<span data-ttu-id="a987d-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a987d-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="a987d-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="a987d-114">Gibt an, ob der Host bei einem Fehler automatisch ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a987d-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="a987d-115">Der Wert ist standardmäßig auf "true" festgelegt, wenn sie nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a987d-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a987d-116">-DefaultProfile</span></span>
<span data-ttu-id="a987d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a987d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a987d-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="a987d-118">-HostGroupName</span></span>
<span data-ttu-id="a987d-119">Gibt den Namen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="a987d-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a987d-120">-LicenseType</span></span>
<span data-ttu-id="a987d-121">Gibt den Softwarelizenztyp an, der auf die auf dem Host bereitgestellten VMs angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a987d-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="a987d-122">Mögliche Werte: "None", "Windows_Server_Hybrid" und "Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="a987d-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="a987d-123">Der Standardwert ist "None".</span><span class="sxs-lookup"><span data-stu-id="a987d-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-124">-Location</span><span class="sxs-lookup"><span data-stu-id="a987d-124">-Location</span></span>
<span data-ttu-id="a987d-125">Gibt den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="a987d-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a987d-126">-Name</span></span>
<span data-ttu-id="a987d-127">Gibt den Namen des Hosts an.</span><span class="sxs-lookup"><span data-stu-id="a987d-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="a987d-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="a987d-129">Gibt die Anzahl der Plattformfehlerdomäne des Hosts an.</span><span class="sxs-lookup"><span data-stu-id="a987d-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="a987d-130">Dann ist der Minimalwert 0 und der Maximalwert 2.</span><span class="sxs-lookup"><span data-stu-id="a987d-130">Then minimum value is 0 and the maximum value is 2.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a987d-131">-ResourceGroupName</span></span>
<span data-ttu-id="a987d-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a987d-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a987d-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="a987d-133">-Sku</span></span>
<span data-ttu-id="a987d-134">Gibt den Namen der SKU an.</span><span class="sxs-lookup"><span data-stu-id="a987d-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="a987d-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="a987d-135">-Tag</span></span>
<span data-ttu-id="a987d-136">Gibt Tags an.</span><span class="sxs-lookup"><span data-stu-id="a987d-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="a987d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a987d-137">-Confirm</span></span>
<span data-ttu-id="a987d-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a987d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a987d-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a987d-139">-WhatIf</span></span>
<span data-ttu-id="a987d-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a987d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a987d-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a987d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a987d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a987d-142">CommonParameters</span></span>
<span data-ttu-id="a987d-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a987d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a987d-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a987d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a987d-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a987d-145">INPUTS</span></span>

### <span data-ttu-id="a987d-146">System.String</span><span class="sxs-lookup"><span data-stu-id="a987d-146">System.String</span></span>

## <span data-ttu-id="a987d-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a987d-147">OUTPUTS</span></span>

### <span data-ttu-id="a987d-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="a987d-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="a987d-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a987d-149">NOTES</span></span>

## <span data-ttu-id="a987d-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a987d-150">RELATED LINKS</span></span>
