---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009164"
---
# <span data-ttu-id="d4cd9-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="d4cd9-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="d4cd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="d4cd9-103">Fortsetzen/erneutes Synchronisieren der Verbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="d4cd9-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="d4cd9-104">Wenn der Vorgang auf dem Quelldatenträger ausgeführt wird, wird die Verbindung wieder synchronisiert, und die Verbindung wird von der Quelle zum Ziel synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="d4cd9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4cd9-105">SYNTAX</span></span>

### <span data-ttu-id="d4cd9-106">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4cd9-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d4cd9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4cd9-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4cd9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4cd9-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4cd9-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4cd9-109">DESCRIPTION</span></span>
<span data-ttu-id="d4cd9-110">Fortsetzen/erneutes Synchronisieren der Verbindung auf dem Zielvolume</span><span class="sxs-lookup"><span data-stu-id="d4cd9-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="d4cd9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4cd9-111">EXAMPLES</span></span>

### <span data-ttu-id="d4cd9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4cd9-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="d4cd9-113">Dieser Befehl setzt die Anf-Replikationsverbindung auf dem Volume "MyDestinationAnfVolume" fort.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="d4cd9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4cd9-114">PARAMETERS</span></span>

### <span data-ttu-id="d4cd9-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d4cd9-115">-AccountName</span></span>
<span data-ttu-id="d4cd9-116">Der Name des ANF-Kontos des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="d4cd9-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="d4cd9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4cd9-117">-DefaultProfile</span></span>
<span data-ttu-id="d4cd9-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4cd9-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4cd9-119">-InputObject</span></span>
<span data-ttu-id="d4cd9-120">Das für die erneute Synchronisierung zu replizierende Zielvolumen Objekt</span><span class="sxs-lookup"><span data-stu-id="d4cd9-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="d4cd9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d4cd9-121">-Name</span></span>
<span data-ttu-id="d4cd9-122">Der Name des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="d4cd9-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d4cd9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4cd9-123">-PassThru</span></span>
<span data-ttu-id="d4cd9-124">Zurückgeben, ob eine erneute Synchronisierung des angegebenen Replikations Datenträgers durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="d4cd9-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="d4cd9-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="d4cd9-125">-PoolName</span></span>
<span data-ttu-id="d4cd9-126">Der Name des ANF-Pools des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="d4cd9-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="d4cd9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4cd9-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4cd9-128">Die Ressourcengruppe des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="d4cd9-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d4cd9-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4cd9-129">-ResourceId</span></span>
<span data-ttu-id="d4cd9-130">Die Ressourcen-ID des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="d4cd9-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="d4cd9-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4cd9-131">-Confirm</span></span>
<span data-ttu-id="d4cd9-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4cd9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4cd9-133">-WhatIf</span></span>
<span data-ttu-id="d4cd9-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4cd9-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4cd9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4cd9-136">CommonParameters</span></span>
<span data-ttu-id="d4cd9-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4cd9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4cd9-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4cd9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4cd9-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4cd9-139">INPUTS</span></span>

### <span data-ttu-id="d4cd9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d4cd9-140">System.String</span></span>

### <span data-ttu-id="d4cd9-141">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d4cd9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="d4cd9-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4cd9-142">OUTPUTS</span></span>

### <span data-ttu-id="d4cd9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4cd9-143">System.Boolean</span></span>

## <span data-ttu-id="d4cd9-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4cd9-144">NOTES</span></span>

## <span data-ttu-id="d4cd9-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4cd9-145">RELATED LINKS</span></span>
