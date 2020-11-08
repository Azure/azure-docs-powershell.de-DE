---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173230"
---
# <span data-ttu-id="93af6-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="93af6-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="93af6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93af6-102">SYNOPSIS</span></span>
<span data-ttu-id="93af6-103">Erstellt eine CustomIpPrefix-Ressource</span><span class="sxs-lookup"><span data-stu-id="93af6-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="93af6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93af6-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93af6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93af6-105">DESCRIPTION</span></span>
<span data-ttu-id="93af6-106">Das Cmdlet **New-AzCustomIpPrefix** erstellt eine CustomIpPrefix-Ressource.</span><span class="sxs-lookup"><span data-stu-id="93af6-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="93af6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93af6-107">EXAMPLES</span></span>

### <span data-ttu-id="93af6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93af6-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="93af6-109">Dieser Befehl erstellt eine neue CustomIpPrefix-Ressource mit dem Namen $prefixName in der Ressourcengruppe $rgName mit einem CIDR von 40.40.40.0/24 in westus.</span><span class="sxs-lookup"><span data-stu-id="93af6-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="93af6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="93af6-110">PARAMETERS</span></span>

### <span data-ttu-id="93af6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93af6-111">-AsJob</span></span>
<span data-ttu-id="93af6-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="93af6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93af6-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="93af6-113">-Cidr</span></span>
<span data-ttu-id="93af6-114">CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="93af6-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="93af6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93af6-115">-DefaultProfile</span></span>
<span data-ttu-id="93af6-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="93af6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93af6-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="93af6-117">-Location</span></span>
<span data-ttu-id="93af6-118">Der CustomIpPrefix-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="93af6-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="93af6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93af6-119">-Name</span></span>
<span data-ttu-id="93af6-120">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="93af6-120">The resource name.</span></span>

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

### <span data-ttu-id="93af6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93af6-121">-ResourceGroupName</span></span>
<span data-ttu-id="93af6-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="93af6-122">The resource group name.</span></span>

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

### <span data-ttu-id="93af6-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="93af6-123">-Tag</span></span>
<span data-ttu-id="93af6-124">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="93af6-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="93af6-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="93af6-125">-Zone</span></span>
<span data-ttu-id="93af6-126">Eine Liste der Verfügbarkeits Zonen, die die IP-Adresse angibt, die für die Ressource reserviert ist, muss stammen.</span><span class="sxs-lookup"><span data-stu-id="93af6-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93af6-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="93af6-127">-Confirm</span></span>
<span data-ttu-id="93af6-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93af6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93af6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93af6-129">-WhatIf</span></span>
<span data-ttu-id="93af6-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93af6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93af6-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93af6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93af6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93af6-132">CommonParameters</span></span>
<span data-ttu-id="93af6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93af6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93af6-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93af6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93af6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93af6-135">INPUTS</span></span>

### <span data-ttu-id="93af6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="93af6-136">System.String</span></span>

### <span data-ttu-id="93af6-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="93af6-137">System.String[]</span></span>

### <span data-ttu-id="93af6-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="93af6-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="93af6-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93af6-139">OUTPUTS</span></span>

### <span data-ttu-id="93af6-140">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="93af6-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="93af6-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="93af6-141">NOTES</span></span>

## <span data-ttu-id="93af6-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93af6-142">RELATED LINKS</span></span>

[<span data-ttu-id="93af6-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="93af6-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="93af6-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="93af6-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="93af6-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="93af6-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)