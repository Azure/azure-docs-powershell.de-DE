---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpPrefix.md
ms.openlocfilehash: d52bc8737392bf6fce004a90b1f2fe5207cffea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664819"
---
# <span data-ttu-id="462ce-101">New-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="462ce-101">New-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="462ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="462ce-102">SYNOPSIS</span></span>
<span data-ttu-id="462ce-103">Erstellt ein öffentliches IP-Präfix</span><span class="sxs-lookup"><span data-stu-id="462ce-103">Creates a Public IP Prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="462ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="462ce-104">SYNTAX</span></span>

```
New-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>]
 [-IpTag <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="462ce-105">DESCRIPTION</span></span>
<span data-ttu-id="462ce-106">Das Cmdlet **New-AzureRmPublicIpPrefix** erstellt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="462ce-106">The **New-AzureRmPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="462ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="462ce-107">EXAMPLES</span></span>

### <span data-ttu-id="462ce-108">1: Erstellen eines neuen öffentlichen IP-Präfixes</span><span class="sxs-lookup"><span data-stu-id="462ce-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="462ce-109">Mit diesem Befehl wird eine neue öffentliche IP-Präfix Ressource erstellt.</span><span class="sxs-lookup"><span data-stu-id="462ce-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="462ce-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="462ce-110">PARAMETERS</span></span>

### <span data-ttu-id="462ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="462ce-111">-AsJob</span></span>
<span data-ttu-id="462ce-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="462ce-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462ce-113">-DefaultProfile</span></span>
<span data-ttu-id="462ce-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="462ce-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-115">-Force</span><span class="sxs-lookup"><span data-stu-id="462ce-115">-Force</span></span>
<span data-ttu-id="462ce-116">Keine Bestätigung anfordern, wenn Sie eine Ressource overriten möchten</span><span class="sxs-lookup"><span data-stu-id="462ce-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="462ce-117">-IpAddressVersion</span></span>
<span data-ttu-id="462ce-118">Die Version der öffentlichen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="462ce-118">The public IP address version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="462ce-119">-IpTag</span></span>
<span data-ttu-id="462ce-120">IpTag-Liste.</span><span class="sxs-lookup"><span data-stu-id="462ce-120">IpTag List.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="462ce-121">-Location</span></span>
<span data-ttu-id="462ce-122">Der Speicherort des öffentlichen IP-Präfixes.</span><span class="sxs-lookup"><span data-stu-id="462ce-122">The public IP prefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-123">-Name</span><span class="sxs-lookup"><span data-stu-id="462ce-123">-Name</span></span>
<span data-ttu-id="462ce-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="462ce-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-125">-Präfixlänge</span><span class="sxs-lookup"><span data-stu-id="462ce-125">-PrefixLength</span></span>
<span data-ttu-id="462ce-126">Die PublicIPPrefix-Länge</span><span class="sxs-lookup"><span data-stu-id="462ce-126">The PublicIPPrefix length</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462ce-127">-ResourceGroupName</span></span>
<span data-ttu-id="462ce-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="462ce-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="462ce-129">-Sku</span></span>
<span data-ttu-id="462ce-130">Der SKU-Name für öffentliche IP-Präfixe.</span><span class="sxs-lookup"><span data-stu-id="462ce-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="462ce-131">-Tag</span></span>
<span data-ttu-id="462ce-132">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="462ce-132">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-133">-Zone</span><span class="sxs-lookup"><span data-stu-id="462ce-133">-Zone</span></span>
<span data-ttu-id="462ce-134">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="462ce-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="462ce-135">-Confirm</span></span>
<span data-ttu-id="462ce-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="462ce-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462ce-137">-WhatIf</span></span>
<span data-ttu-id="462ce-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="462ce-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462ce-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="462ce-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="462ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462ce-140">CommonParameters</span></span>
<span data-ttu-id="462ce-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="462ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="462ce-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462ce-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462ce-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="462ce-143">INPUTS</span></span>

### <span data-ttu-id="462ce-144">System. String</span><span class="sxs-lookup"><span data-stu-id="462ce-144">System.String</span></span>
<span data-ttu-id="462ce-145">System. UInt16 System. Collections. Generic. List `1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="462ce-145">System.UInt16 System.Collections.Generic.List`1[[Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag, Microsoft.Azure.Commands.Network, Version=6.4.0.0, Culture=neutral, PublicKeyToken=null]]
System.Collections.Generic.List`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="462ce-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="462ce-146">OUTPUTS</span></span>

### <span data-ttu-id="462ce-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="462ce-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="462ce-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="462ce-148">NOTES</span></span>

## <span data-ttu-id="462ce-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="462ce-149">RELATED LINKS</span></span>
