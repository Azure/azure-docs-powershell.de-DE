---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165215"
---
# <span data-ttu-id="fd37a-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd37a-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="fd37a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd37a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd37a-103">Erstellt ein öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="fd37a-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="fd37a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd37a-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd37a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd37a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd37a-106">Das Cmdlet **New-AzPublicIpPrefix** erstellt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="fd37a-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="fd37a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd37a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd37a-108">Beispiel 1: Erstellen eines neuen öffentlichen IP-Präfixes</span><span class="sxs-lookup"><span data-stu-id="fd37a-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="fd37a-109">Mit diesem Befehl wird eine neue öffentliche IP-Präfix Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="fd37a-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="fd37a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd37a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd37a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd37a-111">-AsJob</span></span>
<span data-ttu-id="fd37a-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fd37a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fd37a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd37a-113">-DefaultProfile</span></span>
<span data-ttu-id="fd37a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fd37a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd37a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd37a-115">-Force</span></span>
<span data-ttu-id="fd37a-116">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="fd37a-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fd37a-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="fd37a-117">-IpAddressVersion</span></span>
<span data-ttu-id="fd37a-118">Die Version der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="fd37a-118">The public IP address version.</span></span>

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

### <span data-ttu-id="fd37a-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="fd37a-119">-IpTag</span></span>
<span data-ttu-id="fd37a-120">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="fd37a-120">IpTag List.</span></span>

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

### <span data-ttu-id="fd37a-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="fd37a-121">-Location</span></span>
<span data-ttu-id="fd37a-122">Der Speicherort des öffentlichen IP-Präfixes.</span><span class="sxs-lookup"><span data-stu-id="fd37a-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="fd37a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fd37a-123">-Name</span></span>
<span data-ttu-id="fd37a-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fd37a-124">The resource name.</span></span>

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

### <span data-ttu-id="fd37a-125">-Präfixlänge</span><span class="sxs-lookup"><span data-stu-id="fd37a-125">-PrefixLength</span></span>
<span data-ttu-id="fd37a-126">Die PublicIPPrefix-Länge</span><span class="sxs-lookup"><span data-stu-id="fd37a-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="fd37a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd37a-127">-ResourceGroupName</span></span>
<span data-ttu-id="fd37a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fd37a-128">The resource group name.</span></span>

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

### <span data-ttu-id="fd37a-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="fd37a-129">-Sku</span></span>
<span data-ttu-id="fd37a-130">Der SKU-Name für öffentliche IP-Präfixe.</span><span class="sxs-lookup"><span data-stu-id="fd37a-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="fd37a-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="fd37a-131">-Tag</span></span>
<span data-ttu-id="fd37a-132">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="fd37a-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fd37a-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="fd37a-133">-Zone</span></span>
<span data-ttu-id="fd37a-134">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="fd37a-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fd37a-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd37a-135">-Confirm</span></span>
<span data-ttu-id="fd37a-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd37a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd37a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd37a-137">-WhatIf</span></span>
<span data-ttu-id="fd37a-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd37a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd37a-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd37a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd37a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd37a-140">CommonParameters</span></span>
<span data-ttu-id="fd37a-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd37a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd37a-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd37a-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd37a-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd37a-143">INPUTS</span></span>

### <span data-ttu-id="fd37a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd37a-144">System.String</span></span>

### <span data-ttu-id="fd37a-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="fd37a-145">System.UInt16</span></span>

### <span data-ttu-id="fd37a-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="fd37a-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="fd37a-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="fd37a-147">System.String[]</span></span>

### <span data-ttu-id="fd37a-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd37a-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd37a-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd37a-149">OUTPUTS</span></span>

### <span data-ttu-id="fd37a-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd37a-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="fd37a-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd37a-151">NOTES</span></span>

## <span data-ttu-id="fd37a-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd37a-152">RELATED LINKS</span></span>

[<span data-ttu-id="fd37a-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd37a-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="fd37a-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd37a-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="fd37a-155">Satz-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="fd37a-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
