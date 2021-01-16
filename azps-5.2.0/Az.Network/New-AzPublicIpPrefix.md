---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293068"
---
# <span data-ttu-id="15bb4-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="15bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="15bb4-103">Erstellt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="15bb4-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="15bb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15bb4-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15bb4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15bb4-105">DESCRIPTION</span></span>
<span data-ttu-id="15bb4-106">Das **Cmdlet "New-AzPublicIpPrefix"** erstellt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="15bb4-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="15bb4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="15bb4-107">EXAMPLES</span></span>

### <span data-ttu-id="15bb4-108">Beispiel 1: Erstellen eines neuen öffentlichen Ip-Präfixes</span><span class="sxs-lookup"><span data-stu-id="15bb4-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="15bb4-109">Dieser Befehl erstellt eine neue öffentliche IP-Präfixressource.</span><span class="sxs-lookup"><span data-stu-id="15bb4-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="15bb4-110">Beispiel 2: Erstellen eines neuen globalen öffentlichen Ip-Präfixes</span><span class="sxs-lookup"><span data-stu-id="15bb4-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="15bb4-111">Mit diesem Befehl wird eine neue globale Öffentliche IP-Präfixressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="15bb4-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="15bb4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15bb4-112">PARAMETERS</span></span>

### <span data-ttu-id="15bb4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15bb4-113">-AsJob</span></span>
<span data-ttu-id="15bb4-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="15bb4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15bb4-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-115">-CustomIpPrefix</span></span>
<span data-ttu-id="15bb4-116">Das CustomIpPrefix, dem dieses PublicIpPrefix zugeordnet wird</span><span class="sxs-lookup"><span data-stu-id="15bb4-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15bb4-117">-DefaultProfile</span></span>
<span data-ttu-id="15bb4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="15bb4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15bb4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="15bb4-119">-Force</span></span>
<span data-ttu-id="15bb4-120">Bestätigen Sie sie nicht, wenn Sie eine Ressource überschreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="15bb4-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="15bb4-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="15bb4-121">-IpAddressVersion</span></span>
<span data-ttu-id="15bb4-122">Die Version der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="15bb4-122">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="15bb4-123">-IpTag</span></span>
<span data-ttu-id="15bb4-124">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="15bb4-124">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="15bb4-125">-Location</span></span>
<span data-ttu-id="15bb4-126">Der Speicherort des öffentlichen IP-Präfixes.</span><span class="sxs-lookup"><span data-stu-id="15bb4-126">The public IP prefix location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="15bb4-127">-Name</span></span>
<span data-ttu-id="15bb4-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="15bb4-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="15bb4-129">-PrefixLength</span></span>
<span data-ttu-id="15bb4-130">Die Länge von PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-130">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15bb4-131">-ResourceGroupName</span></span>
<span data-ttu-id="15bb4-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="15bb4-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="15bb4-133">-Sku</span></span>
<span data-ttu-id="15bb4-134">Der Name des öffentlichen IP-Präfix-SKU.</span><span class="sxs-lookup"><span data-stu-id="15bb4-134">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="15bb4-135">-Tag</span></span>
<span data-ttu-id="15bb4-136">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="15bb4-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="15bb4-137">-Tier</span></span>
<span data-ttu-id="15bb4-138">Die öffentlichen IP-Präfix-SKU-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="15bb4-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="15bb4-139">-Zone</span></span>
<span data-ttu-id="15bb4-140">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugeordnete IP aufgeführt wird, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="15bb4-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15bb4-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15bb4-141">-Confirm</span></span>
<span data-ttu-id="15bb4-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15bb4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15bb4-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="15bb4-143">-WhatIf</span></span>
<span data-ttu-id="15bb4-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15bb4-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15bb4-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15bb4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15bb4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15bb4-146">CommonParameters</span></span>
<span data-ttu-id="15bb4-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15bb4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15bb4-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15bb4-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15bb4-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="15bb4-149">INPUTS</span></span>

### <span data-ttu-id="15bb4-150">System.String</span><span class="sxs-lookup"><span data-stu-id="15bb4-150">System.String</span></span>

### <span data-ttu-id="15bb4-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="15bb4-151">System.UInt16</span></span>

### <span data-ttu-id="15bb4-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="15bb4-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="15bb4-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="15bb4-153">System.String[]</span></span>

### <span data-ttu-id="15bb4-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="15bb4-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="15bb4-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="15bb4-155">OUTPUTS</span></span>

### <span data-ttu-id="15bb4-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="15bb4-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="15bb4-157">NOTES</span></span>

## <span data-ttu-id="15bb4-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="15bb4-158">RELATED LINKS</span></span>

[<span data-ttu-id="15bb4-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="15bb4-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="15bb4-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="15bb4-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
