---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/suspend-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Suspend-AzNetAppFilesReplication.md
ms.openlocfilehash: eb695da1dc1fea238a57ea1c98bec42899e8f28f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303169"
---
# <span data-ttu-id="65096-101">Suspend-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="65096-101">Suspend-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="65096-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65096-102">SYNOPSIS</span></span>
<span data-ttu-id="65096-103">Anhalten/Aufheben der Replikationsverbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="65096-103">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="65096-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65096-104">SYNTAX</span></span>

### <span data-ttu-id="65096-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="65096-105">ByFieldsParameterSet (Default)</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65096-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65096-106">ByResourceIdParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65096-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65096-107">ByObjectParameterSet</span></span>
```
Suspend-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65096-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65096-108">DESCRIPTION</span></span>
<span data-ttu-id="65096-109">Anhalten/Aufheben der Replikationsverbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="65096-109">Suspend/break the replication connection on the destination volume</span></span>

## <span data-ttu-id="65096-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65096-110">EXAMPLES</span></span>

### <span data-ttu-id="65096-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65096-111">Example 1</span></span>
```powershell
PS C:\> Suspend-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="65096-112">Dieser Befehl unterbricht die Anf-Replikationsverbindung auf dem Volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="65096-112">This command suspends the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="65096-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="65096-113">PARAMETERS</span></span>

### <span data-ttu-id="65096-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="65096-114">-AccountName</span></span>
<span data-ttu-id="65096-115">Der Name des ANF-Kontos des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="65096-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="65096-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65096-116">-DefaultProfile</span></span>
<span data-ttu-id="65096-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65096-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65096-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="65096-118">-InputObject</span></span>
<span data-ttu-id="65096-119">Das ANF-Zielvolumen Objekt mit der zu unterbrechenden Replikation</span><span class="sxs-lookup"><span data-stu-id="65096-119">The ANF destination volume object with the replication to break</span></span>

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

### <span data-ttu-id="65096-120">-Name</span><span class="sxs-lookup"><span data-stu-id="65096-120">-Name</span></span>
<span data-ttu-id="65096-121">Der Name des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="65096-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="65096-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65096-122">-PassThru</span></span>
<span data-ttu-id="65096-123">Gibt zurück, ob die Unterbrechung der angegebenen Volume-Replikation durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="65096-123">Return whether the break of the specified volume replication was performed</span></span>

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

### <span data-ttu-id="65096-124">-Poolname</span><span class="sxs-lookup"><span data-stu-id="65096-124">-PoolName</span></span>
<span data-ttu-id="65096-125">Der Name des ANF-Pools des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="65096-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="65096-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65096-126">-ResourceGroupName</span></span>
<span data-ttu-id="65096-127">Die Ressourcengruppe des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="65096-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="65096-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="65096-128">-ResourceId</span></span>
<span data-ttu-id="65096-129">Die Ressourcen-ID des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="65096-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="65096-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="65096-130">-Confirm</span></span>
<span data-ttu-id="65096-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="65096-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65096-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65096-132">-WhatIf</span></span>
<span data-ttu-id="65096-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="65096-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65096-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="65096-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65096-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65096-135">CommonParameters</span></span>
<span data-ttu-id="65096-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65096-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65096-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65096-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65096-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65096-138">INPUTS</span></span>

### <span data-ttu-id="65096-139">System. String</span><span class="sxs-lookup"><span data-stu-id="65096-139">System.String</span></span>

### <span data-ttu-id="65096-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="65096-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="65096-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65096-141">OUTPUTS</span></span>

### <span data-ttu-id="65096-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65096-142">System.Boolean</span></span>

## <span data-ttu-id="65096-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="65096-143">NOTES</span></span>

## <span data-ttu-id="65096-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65096-144">RELATED LINKS</span></span>
