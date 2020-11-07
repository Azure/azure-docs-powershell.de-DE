---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHostGroup.md
ms.openlocfilehash: 9d6614204c8c6e8e95617ed989e3f75b88c9744e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652076"
---
# <span data-ttu-id="13ec5-101">New-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="13ec5-101">New-AzHostGroup</span></span>

## <span data-ttu-id="13ec5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13ec5-102">SYNOPSIS</span></span>
<span data-ttu-id="13ec5-103">Erstellt eine Hostgruppe.</span><span class="sxs-lookup"><span data-stu-id="13ec5-103">Creates a host group.</span></span>

## <span data-ttu-id="13ec5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13ec5-104">SYNTAX</span></span>

```
New-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 -PlatformFaultDomain <Int32> [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13ec5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13ec5-105">DESCRIPTION</span></span>
<span data-ttu-id="13ec5-106">Mit diesem Cmdlet wird eine Host Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="13ec5-106">This cmdlet will create a Host group.</span></span>

## <span data-ttu-id="13ec5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13ec5-107">EXAMPLES</span></span>

### <span data-ttu-id="13ec5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13ec5-108">Example 1</span></span>
```
PS C:\> New-AzHostGroup -ResourceGroupName $resourceGroupName -Name $hostGroupName -Location $location -Zone $zone

ResourceGroupName        : myrg01
PlatformFaultDomainCount : 2
Hosts                    : {/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01}
Zones                    : {1}
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01
Name                     : myhostgroup01
Location                 : eastus
Tags                     : {[key1, val1]}
```

<span data-ttu-id="13ec5-109">Dieser Befehl erstellt eine Hostgruppe in der angegebenen Position und Zone.</span><span class="sxs-lookup"><span data-stu-id="13ec5-109">This command creates a host group in the given location and zone.</span></span>

## <span data-ttu-id="13ec5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="13ec5-110">PARAMETERS</span></span>

### <span data-ttu-id="13ec5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13ec5-111">-AsJob</span></span>
<span data-ttu-id="13ec5-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="13ec5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13ec5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13ec5-113">-DefaultProfile</span></span>
<span data-ttu-id="13ec5-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13ec5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13ec5-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="13ec5-115">-Location</span></span>
<span data-ttu-id="13ec5-116">Gibt die Position an.</span><span class="sxs-lookup"><span data-stu-id="13ec5-116">Specifies location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="13ec5-117">-Name</span></span>
<span data-ttu-id="13ec5-118">Gibt den Namen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="13ec5-118">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-119">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="13ec5-119">-PlatformFaultDomain</span></span>
<span data-ttu-id="13ec5-120">Gibt die Anzahl der fehlerdomänen an, die die Hostgruppe überspannen kann.</span><span class="sxs-lookup"><span data-stu-id="13ec5-120">Specifies the number of fault domains that the host group can span.</span></span>  <span data-ttu-id="13ec5-121">Der Mindestwert ist 1, und der Höchstwert ist 3.</span><span class="sxs-lookup"><span data-stu-id="13ec5-121">The minimum value is 1 and the maximum value is 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13ec5-122">-ResourceGroupName</span></span>
<span data-ttu-id="13ec5-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="13ec5-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="13ec5-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="13ec5-124">-Tag</span></span>
<span data-ttu-id="13ec5-125">Gibt Tags an</span><span class="sxs-lookup"><span data-stu-id="13ec5-125">Specifies Tags</span></span>

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

### <span data-ttu-id="13ec5-126">-Zone</span><span class="sxs-lookup"><span data-stu-id="13ec5-126">-Zone</span></span>
<span data-ttu-id="13ec5-127">Gibt Zonen der Hostgruppe an.</span><span class="sxs-lookup"><span data-stu-id="13ec5-127">Specifies Zones of the host group.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13ec5-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="13ec5-128">-Confirm</span></span>
<span data-ttu-id="13ec5-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13ec5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13ec5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13ec5-130">-WhatIf</span></span>
<span data-ttu-id="13ec5-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13ec5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13ec5-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13ec5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13ec5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13ec5-133">CommonParameters</span></span>
<span data-ttu-id="13ec5-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13ec5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13ec5-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13ec5-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13ec5-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13ec5-136">INPUTS</span></span>

### <span data-ttu-id="13ec5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="13ec5-137">System.String</span></span>

## <span data-ttu-id="13ec5-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13ec5-138">OUTPUTS</span></span>

### <span data-ttu-id="13ec5-139">Microsoft. Azure. Commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="13ec5-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="13ec5-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="13ec5-140">NOTES</span></span>

## <span data-ttu-id="13ec5-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13ec5-141">RELATED LINKS</span></span>
