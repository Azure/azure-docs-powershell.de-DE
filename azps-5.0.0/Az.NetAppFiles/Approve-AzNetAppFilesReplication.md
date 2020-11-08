---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178598"
---
# <span data-ttu-id="717b7-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="717b7-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="717b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="717b7-102">SYNOPSIS</span></span>
<span data-ttu-id="717b7-103">Genehmigen/Autorisieren der Replikationsverbindung auf dem Quelldatenträger</span><span class="sxs-lookup"><span data-stu-id="717b7-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="717b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="717b7-104">SYNTAX</span></span>

### <span data-ttu-id="717b7-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="717b7-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="717b7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="717b7-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="717b7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="717b7-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="717b7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="717b7-108">DESCRIPTION</span></span>
<span data-ttu-id="717b7-109">Genehmigen der Replikationsverbindung auf dem Quelldatenträger</span><span class="sxs-lookup"><span data-stu-id="717b7-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="717b7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="717b7-110">EXAMPLES</span></span>

### <span data-ttu-id="717b7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="717b7-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="717b7-112">Dieser Befehl genehmigt die Replikation auf MyAnfVolume.</span><span class="sxs-lookup"><span data-stu-id="717b7-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="717b7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="717b7-113">PARAMETERS</span></span>

### <span data-ttu-id="717b7-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="717b7-114">-AccountName</span></span>
<span data-ttu-id="717b7-115">Der Name des ANF-Kontos des Replikations Quelldatenträgers</span><span class="sxs-lookup"><span data-stu-id="717b7-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="717b7-116">-DataProtectionVolumeId</span><span class="sxs-lookup"><span data-stu-id="717b7-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="717b7-117">Die Dateisystem-ID des Ziel Datenschutz-Volumes</span><span class="sxs-lookup"><span data-stu-id="717b7-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="717b7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717b7-118">-DefaultProfile</span></span>
<span data-ttu-id="717b7-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="717b7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="717b7-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="717b7-120">-InputObject</span></span>
<span data-ttu-id="717b7-121">Das ANF-Quellvolumen Objekt, das das Replikationsziel autorisiert hat</span><span class="sxs-lookup"><span data-stu-id="717b7-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="717b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="717b7-122">-Name</span></span>
<span data-ttu-id="717b7-123">Der Name des ANF-Replikations Quelldatenträgers</span><span class="sxs-lookup"><span data-stu-id="717b7-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="717b7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="717b7-124">-PassThru</span></span>
<span data-ttu-id="717b7-125">Gibt zurück, ob die Replikations Autorisierung des angegebenen Volumes durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="717b7-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="717b7-126">-Poolname</span><span class="sxs-lookup"><span data-stu-id="717b7-126">-PoolName</span></span>
<span data-ttu-id="717b7-127">Der Name des ANF-Pools des Replikations Quelldatenträgers</span><span class="sxs-lookup"><span data-stu-id="717b7-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="717b7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="717b7-128">-ResourceGroupName</span></span>
<span data-ttu-id="717b7-129">Die Ressourcengruppe des ANF-Replikations Quelldatenträgers</span><span class="sxs-lookup"><span data-stu-id="717b7-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="717b7-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="717b7-130">-ResourceId</span></span>
<span data-ttu-id="717b7-131">Die Ressourcen-ID des ANF-Replikations Quelldatenträgers</span><span class="sxs-lookup"><span data-stu-id="717b7-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="717b7-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="717b7-132">-Confirm</span></span>
<span data-ttu-id="717b7-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="717b7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717b7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717b7-134">-WhatIf</span></span>
<span data-ttu-id="717b7-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="717b7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717b7-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="717b7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717b7-137">CommonParameters</span></span>
<span data-ttu-id="717b7-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="717b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717b7-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717b7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717b7-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="717b7-140">INPUTS</span></span>

### <span data-ttu-id="717b7-141">System. String</span><span class="sxs-lookup"><span data-stu-id="717b7-141">System.String</span></span>

### <span data-ttu-id="717b7-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="717b7-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="717b7-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="717b7-143">OUTPUTS</span></span>

### <span data-ttu-id="717b7-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="717b7-144">System.Boolean</span></span>

## <span data-ttu-id="717b7-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="717b7-145">NOTES</span></span>

## <span data-ttu-id="717b7-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="717b7-146">RELATED LINKS</span></span>
