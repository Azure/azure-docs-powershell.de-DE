---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179391"
---
# <span data-ttu-id="f59ad-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f59ad-101">Remove-AzPeering</span></span>

## <span data-ttu-id="f59ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f59ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f59ad-103">Löschen oder Entfernen eines Peerings</span><span class="sxs-lookup"><span data-stu-id="f59ad-103">Delete or remove a peering.</span></span> <span data-ttu-id="f59ad-104">Dadurch werden alle untergeordneten Ressourcen oder Warnungen für die Ressource gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f59ad-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="f59ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f59ad-105">SYNTAX</span></span>

### <span data-ttu-id="f59ad-106">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f59ad-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59ad-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f59ad-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59ad-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f59ad-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f59ad-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f59ad-109">DESCRIPTION</span></span>
<span data-ttu-id="f59ad-110">Perminently Löschen einer Peering-Ressource.</span><span class="sxs-lookup"><span data-stu-id="f59ad-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="f59ad-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f59ad-111">EXAMPLES</span></span>

### <span data-ttu-id="f59ad-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f59ad-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="f59ad-113">Entfernen Sie ein Peering nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f59ad-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="f59ad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f59ad-114">PARAMETERS</span></span>

### <span data-ttu-id="f59ad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f59ad-115">-AsJob</span></span>
<span data-ttu-id="f59ad-116">Im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f59ad-116">Run in the background.</span></span>

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

### <span data-ttu-id="f59ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59ad-117">-DefaultProfile</span></span>
<span data-ttu-id="f59ad-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f59ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59ad-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f59ad-119">-Force</span></span>
<span data-ttu-id="f59ad-120">Erzwingen der Ausführung des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="f59ad-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="f59ad-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f59ad-121">-InputObject</span></span>
<span data-ttu-id="f59ad-122">Verwenden Sie Get-AzPeering, um dieses Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f59ad-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ad-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f59ad-123">-Name</span></span>
<span data-ttu-id="f59ad-124">Der eindeutige Name des PSPeering.</span><span class="sxs-lookup"><span data-stu-id="f59ad-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f59ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f59ad-125">-PassThru</span></span>
<span data-ttu-id="f59ad-126">True zurück, wenn abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="f59ad-126">Return true if complete</span></span>

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

### <span data-ttu-id="f59ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="f59ad-128">Der Name der vorhandenen Ressourcengruppe erstellen oder verwenden</span><span class="sxs-lookup"><span data-stu-id="f59ad-128">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f59ad-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f59ad-129">-ResourceId</span></span>
<span data-ttu-id="f59ad-130">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f59ad-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ad-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f59ad-131">-Confirm</span></span>
<span data-ttu-id="f59ad-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f59ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59ad-133">-WhatIf</span></span>
<span data-ttu-id="f59ad-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f59ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59ad-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f59ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59ad-136">CommonParameters</span></span>
<span data-ttu-id="f59ad-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f59ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59ad-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f59ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59ad-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f59ad-139">INPUTS</span></span>

### <span data-ttu-id="f59ad-140">Microsoft. Azure. PowerShell. Cmdlets. Peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f59ad-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="f59ad-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f59ad-141">System.String</span></span>

## <span data-ttu-id="f59ad-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f59ad-142">OUTPUTS</span></span>

### <span data-ttu-id="f59ad-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f59ad-143">System.Boolean</span></span>

## <span data-ttu-id="f59ad-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="f59ad-144">NOTES</span></span>

## <span data-ttu-id="f59ad-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f59ad-145">RELATED LINKS</span></span>
