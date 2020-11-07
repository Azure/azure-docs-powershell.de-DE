---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringServicePrefix.md
ms.openlocfilehash: 36003d1fbca7566ae663a1d878386f3d8d67f484
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824000"
---
# <span data-ttu-id="5e167-101">Remove-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5e167-101">Remove-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="5e167-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e167-102">SYNOPSIS</span></span>
<span data-ttu-id="5e167-103">Entfernt ein neues Peering-Dienst Präfix</span><span class="sxs-lookup"><span data-stu-id="5e167-103">Removes a new peering service prefix</span></span>

## <span data-ttu-id="5e167-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e167-104">SYNTAX</span></span>

### <span data-ttu-id="5e167-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e167-105">ByName (Default)</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceGroupName] <String> [-Name] <String> [-PeeringServiceName] <String>
 [-Force] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e167-106">Standard</span><span class="sxs-lookup"><span data-stu-id="5e167-106">Default</span></span>
```
Remove-AzPeeringServicePrefix -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e167-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e167-107">ByResourceId</span></span>
```
Remove-AzPeeringServicePrefix [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e167-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e167-108">DESCRIPTION</span></span>
<span data-ttu-id="5e167-109">Entfernt ein Peering-Dienst Präfix von einem peeringdienst.</span><span class="sxs-lookup"><span data-stu-id="5e167-109">Removes a peering service prefix from a peering service.</span></span>

## <span data-ttu-id="5e167-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e167-110">EXAMPLES</span></span>

### <span data-ttu-id="5e167-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e167-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | Remove-AzPeeringServicePrefix -Name $prefixName
```

<span data-ttu-id="5e167-112">Entfernen eines Präfixes aus einem Peering-Dienstobjekt</span><span class="sxs-lookup"><span data-stu-id="5e167-112">Remove a prefix from a peering service object</span></span>

### <span data-ttu-id="5e167-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5e167-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceId $peeringServiceResourceId -Name $prefixName -PassThru

True
```

<span data-ttu-id="5e167-114">Entfernen Sie ein Präfix aus der Ressourcen-ID des Peering-Diensts.</span><span class="sxs-lookup"><span data-stu-id="5e167-114">Remove a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="5e167-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="5e167-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -PassThru

True
```

<span data-ttu-id="5e167-116">Entfernen eines Präfixes aus dem Namen und Namen einer peeringdienst-Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5e167-116">Remove a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="5e167-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e167-117">PARAMETERS</span></span>

### <span data-ttu-id="5e167-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e167-118">-AsJob</span></span>
<span data-ttu-id="5e167-119">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5e167-119">Run in the background.</span></span>

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

### <span data-ttu-id="5e167-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e167-120">-DefaultProfile</span></span>
<span data-ttu-id="5e167-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e167-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e167-122">-Force</span><span class="sxs-lookup"><span data-stu-id="5e167-122">-Force</span></span>
<span data-ttu-id="5e167-123">Erzwingen der Ausführung des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="5e167-123">Force the operation to complete</span></span>

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

### <span data-ttu-id="5e167-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e167-124">-InputObject</span></span>
<span data-ttu-id="5e167-125">Verwenden eines Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5e167-125">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5e167-126">-Name</span></span>
<span data-ttu-id="5e167-127">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5e167-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e167-128">-PassThru</span></span>
<span data-ttu-id="5e167-129">Gibt "true" für "Erfolg" oder "falsch" für Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5e167-129">Returns true for success or false for failed.</span></span>

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

### <span data-ttu-id="5e167-130">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="5e167-130">-PeeringServiceName</span></span>
<span data-ttu-id="5e167-131">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="5e167-131">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e167-132">-ResourceGroupName</span></span>
<span data-ttu-id="5e167-133">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="5e167-133">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e167-134">-ResourceId</span></span>
<span data-ttu-id="5e167-135">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e167-135">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e167-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e167-136">-Confirm</span></span>
<span data-ttu-id="5e167-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e167-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e167-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e167-138">-WhatIf</span></span>
<span data-ttu-id="5e167-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e167-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e167-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e167-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e167-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e167-141">CommonParameters</span></span>
<span data-ttu-id="5e167-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e167-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e167-143">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e167-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e167-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e167-144">INPUTS</span></span>

### <span data-ttu-id="5e167-145">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="5e167-145">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="5e167-146">System. String</span><span class="sxs-lookup"><span data-stu-id="5e167-146">System.String</span></span>

## <span data-ttu-id="5e167-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e167-147">OUTPUTS</span></span>

### <span data-ttu-id="5e167-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e167-148">System.Boolean</span></span>

## <span data-ttu-id="5e167-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e167-149">NOTES</span></span>

## <span data-ttu-id="5e167-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e167-150">RELATED LINKS</span></span>
