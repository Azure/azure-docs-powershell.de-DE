---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: c72c4ad67f6096f5ba86924219670be53a725d26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919563"
---
# <span data-ttu-id="e00e7-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="e00e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e00e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e00e7-103">Erstellt ein öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="e00e7-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="e00e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e00e7-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e00e7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e00e7-105">DESCRIPTION</span></span>
<span data-ttu-id="e00e7-106">Das **Cmdlet New-AzPublicIpPrefix** erstellt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="e00e7-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="e00e7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e00e7-107">EXAMPLES</span></span>

### <span data-ttu-id="e00e7-108">Beispiel 1: Erstellen eines neuen öffentlichen Ip-Präfixes</span><span class="sxs-lookup"><span data-stu-id="e00e7-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="e00e7-109">Mit diesem Befehl wird eine neue öffentliche IP-Präfixressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="e00e7-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="e00e7-110">Beispiel 2: Erstellen eines neuen globalen öffentlichen Ip-Präfixes</span><span class="sxs-lookup"><span data-stu-id="e00e7-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="e00e7-111">Mit diesem Befehl wird eine neue globale öffentliche IP-Präfixressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="e00e7-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="e00e7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e00e7-112">PARAMETERS</span></span>

### <span data-ttu-id="e00e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e00e7-113">-AsJob</span></span>
<span data-ttu-id="e00e7-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e00e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e00e7-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-115">-CustomIpPrefix</span></span>
<span data-ttu-id="e00e7-116">Das CustomIpPrefix, dem dieses PublicIpPrefix zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="e00e7-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

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

### <span data-ttu-id="e00e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e00e7-117">-DefaultProfile</span></span>
<span data-ttu-id="e00e7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e00e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e00e7-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="e00e7-119">-Force</span></span>
<span data-ttu-id="e00e7-120">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="e00e7-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e00e7-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="e00e7-121">-IpAddressVersion</span></span>
<span data-ttu-id="e00e7-122">Die Version der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="e00e7-122">The public IP address version.</span></span>

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

### <span data-ttu-id="e00e7-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="e00e7-123">-IpTag</span></span>
<span data-ttu-id="e00e7-124">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="e00e7-124">IpTag List.</span></span>

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

### <span data-ttu-id="e00e7-125">-Location</span><span class="sxs-lookup"><span data-stu-id="e00e7-125">-Location</span></span>
<span data-ttu-id="e00e7-126">Der öffentliche IP-Präfixspeicherort.</span><span class="sxs-lookup"><span data-stu-id="e00e7-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="e00e7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e00e7-127">-Name</span></span>
<span data-ttu-id="e00e7-128">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="e00e7-128">The resource name.</span></span>

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

### <span data-ttu-id="e00e7-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="e00e7-129">-PrefixLength</span></span>
<span data-ttu-id="e00e7-130">Die PublicIPPrefix-Länge</span><span class="sxs-lookup"><span data-stu-id="e00e7-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="e00e7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e00e7-131">-ResourceGroupName</span></span>
<span data-ttu-id="e00e7-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e00e7-132">The resource group name.</span></span>

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

### <span data-ttu-id="e00e7-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="e00e7-133">-Sku</span></span>
<span data-ttu-id="e00e7-134">Der name der öffentlichen IP-Präfix-Sku.</span><span class="sxs-lookup"><span data-stu-id="e00e7-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="e00e7-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="e00e7-135">-Tag</span></span>
<span data-ttu-id="e00e7-136">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="e00e7-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e00e7-137">-Tier</span><span class="sxs-lookup"><span data-stu-id="e00e7-137">-Tier</span></span>
<span data-ttu-id="e00e7-138">Die öffentliche IP-Präfix-Sku-Ebene.</span><span class="sxs-lookup"><span data-stu-id="e00e7-138">The public IP Prefix Sku tier.</span></span>

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

### <span data-ttu-id="e00e7-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="e00e7-139">-Zone</span></span>
<span data-ttu-id="e00e7-140">Eine Liste der Verfügbarkeitszonen, in der die für die Ressource zugewiesene IP bezeichnet wird, muss von stammen.</span><span class="sxs-lookup"><span data-stu-id="e00e7-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="e00e7-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e00e7-141">-Confirm</span></span>
<span data-ttu-id="e00e7-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e00e7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e00e7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e00e7-143">-WhatIf</span></span>
<span data-ttu-id="e00e7-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e00e7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e00e7-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e00e7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e00e7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e00e7-146">CommonParameters</span></span>
<span data-ttu-id="e00e7-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e00e7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e00e7-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e00e7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e00e7-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e00e7-149">INPUTS</span></span>

### <span data-ttu-id="e00e7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="e00e7-150">System.String</span></span>

### <span data-ttu-id="e00e7-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="e00e7-151">System.UInt16</span></span>

### <span data-ttu-id="e00e7-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="e00e7-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="e00e7-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e00e7-153">System.String[]</span></span>

### <span data-ttu-id="e00e7-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e00e7-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e00e7-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e00e7-155">OUTPUTS</span></span>

### <span data-ttu-id="e00e7-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="e00e7-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e00e7-157">NOTES</span></span>

## <span data-ttu-id="e00e7-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e00e7-158">RELATED LINKS</span></span>

[<span data-ttu-id="e00e7-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="e00e7-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="e00e7-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e00e7-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
