---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: ab4d79b4770f438b233e5bfcc740e79364955ea6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298720"
---
# <span data-ttu-id="5c2f3-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="5c2f3-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="5c2f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2f3-103">Anhalten/Anhalten der Replikationsverbindung für das Zielvolume</span><span class="sxs-lookup"><span data-stu-id="5c2f3-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="5c2f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c2f3-104">SYNTAX</span></span>

### <span data-ttu-id="5c2f3-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5c2f3-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-ForceBreak] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c2f3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c2f3-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c2f3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c2f3-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c2f3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c2f3-108">DESCRIPTION</span></span>
<span data-ttu-id="5c2f3-109">Anhalten/Anhalten der Replikationsverbindung für das Zielvolume</span><span class="sxs-lookup"><span data-stu-id="5c2f3-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="5c2f3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c2f3-110">EXAMPLES</span></span>

### <span data-ttu-id="5c2f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5c2f3-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="5c2f3-112">Mit diesem Befehl wird die Verbindung für die ANF-Replikation auf Volume "MyDestinationAnfVolume" angehalten.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="5c2f3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c2f3-113">PARAMETERS</span></span>

### <span data-ttu-id="5c2f3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5c2f3-114">-AccountName</span></span>
<span data-ttu-id="5c2f3-115">Der Name des ANF-Kontos des Replikationsvolumes</span><span class="sxs-lookup"><span data-stu-id="5c2f3-115">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2f3-116">-DefaultProfile</span></span>
<span data-ttu-id="5c2f3-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2f3-118">-ForceBreak</span><span class="sxs-lookup"><span data-stu-id="5c2f3-118">-ForceBreak</span></span>
<span data-ttu-id="5c2f3-119">Wenn die Replikation im Status übertragen wird und Sie eine Unterbrechung der Replikation erzwingen möchten, wird diese auf "true" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-119">If replication is in status transferring and you want to force break the replication, set to true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c2f3-120">-InputObject</span></span>
<span data-ttu-id="5c2f3-121">Das ANF-Zielvolumeobjekt mit der zu brechende Replikation</span><span class="sxs-lookup"><span data-stu-id="5c2f3-121">The ANF destination volume object with the replication to break</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5c2f3-122">-Name</span></span>
<span data-ttu-id="5c2f3-123">Der Name des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5c2f3-123">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c2f3-124">-PassThru</span></span>
<span data-ttu-id="5c2f3-125">Gibt zurück, ob die Unterbrechung der angegebenen Volumenreplikation ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-125">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="5c2f3-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5c2f3-126">-PoolName</span></span>
<span data-ttu-id="5c2f3-127">Der Name des ANF-Pools des Replikationsvolumens</span><span class="sxs-lookup"><span data-stu-id="5c2f3-127">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2f3-128">-ResourceGroupName</span></span>
<span data-ttu-id="5c2f3-129">Die Ressourcengruppe des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5c2f3-129">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c2f3-130">-ResourceId</span></span>
<span data-ttu-id="5c2f3-131">Die Ressourcen-ID des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5c2f3-131">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c2f3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c2f3-132">-Confirm</span></span>
<span data-ttu-id="5c2f3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c2f3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5c2f3-134">-WhatIf</span></span>
<span data-ttu-id="5c2f3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c2f3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c2f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2f3-137">CommonParameters</span></span>
<span data-ttu-id="5c2f3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c2f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2f3-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c2f3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2f3-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c2f3-140">INPUTS</span></span>

### <span data-ttu-id="5c2f3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2f3-141">System.String</span></span>

### <span data-ttu-id="5c2f3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5c2f3-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5c2f3-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c2f3-143">OUTPUTS</span></span>

### <span data-ttu-id="5c2f3-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c2f3-144">System.Boolean</span></span>

## <span data-ttu-id="5c2f3-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5c2f3-145">NOTES</span></span>

## <span data-ttu-id="5c2f3-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5c2f3-146">RELATED LINKS</span></span>
