---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475618"
---
# <span data-ttu-id="c917b-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="c917b-101">New-AzsIpPool</span></span>

## <span data-ttu-id="c917b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c917b-102">SYNOPSIS</span></span>
<span data-ttu-id="c917b-103">Erstellen eines IP-infrastrukturpools</span><span class="sxs-lookup"><span data-stu-id="c917b-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="c917b-104">Nach dem Erstellen eines IP-Pools kann nicht gelöscht oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c917b-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="c917b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c917b-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c917b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c917b-106">DESCRIPTION</span></span>
<span data-ttu-id="c917b-107">Erstellen eines IP-infrastrukturpools</span><span class="sxs-lookup"><span data-stu-id="c917b-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="c917b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c917b-108">EXAMPLES</span></span>

### <span data-ttu-id="c917b-109">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c917b-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="c917b-110">Erstellen Sie einen neuen IP-Pool.</span><span class="sxs-lookup"><span data-stu-id="c917b-110">Create a new IP pool.</span></span>

## <span data-ttu-id="c917b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c917b-111">PARAMETERS</span></span>

### <span data-ttu-id="c917b-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c917b-112">-AddressPrefix</span></span>
<span data-ttu-id="c917b-113">Das Adresspräfix.</span><span class="sxs-lookup"><span data-stu-id="c917b-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c917b-114">-AsJob</span></span>
<span data-ttu-id="c917b-115">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c917b-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c917b-116">-EndIpAddress</span></span>
<span data-ttu-id="c917b-117">Die letzte IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c917b-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="c917b-118">-Location</span></span>
<span data-ttu-id="c917b-119">Der Bereich, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c917b-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c917b-120">-Name</span></span>
<span data-ttu-id="c917b-121">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="c917b-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c917b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c917b-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c917b-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c917b-124">-StartIpAddress</span></span>
<span data-ttu-id="c917b-125">Die Start-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c917b-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="c917b-126">-Tags</span></span>
<span data-ttu-id="c917b-127">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="c917b-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c917b-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c917b-128">-Confirm</span></span>
<span data-ttu-id="c917b-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c917b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c917b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c917b-130">-WhatIf</span></span>
<span data-ttu-id="c917b-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c917b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c917b-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c917b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c917b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c917b-133">CommonParameters</span></span>
<span data-ttu-id="c917b-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c917b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c917b-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c917b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c917b-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c917b-136">INPUTS</span></span>

## <span data-ttu-id="c917b-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c917b-137">OUTPUTS</span></span>

### <span data-ttu-id="c917b-138">Microsoft. AzureStack. Management. Fabric. admin. Models. ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="c917b-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="c917b-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c917b-139">NOTES</span></span>

## <span data-ttu-id="c917b-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c917b-140">RELATED LINKS</span></span>

