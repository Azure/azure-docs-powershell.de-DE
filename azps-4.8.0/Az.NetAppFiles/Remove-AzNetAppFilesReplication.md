---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166324"
---
# <span data-ttu-id="4347f-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="4347f-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="4347f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4347f-102">SYNOPSIS</span></span>
<span data-ttu-id="4347f-103">Entfernen/Löschen der Replikationsverbindung auf dem Zieldatenträger und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="4347f-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="4347f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4347f-104">SYNTAX</span></span>

### <span data-ttu-id="4347f-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4347f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4347f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4347f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4347f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4347f-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4347f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4347f-108">DESCRIPTION</span></span>
<span data-ttu-id="4347f-109">Entfernen/Löschen der Replikationsverbindung auf dem Zieldatenträger und Senden der Freigabe an die Quellreplikation</span><span class="sxs-lookup"><span data-stu-id="4347f-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="4347f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4347f-110">EXAMPLES</span></span>

### <span data-ttu-id="4347f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4347f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="4347f-112">Dieser Befehl entfernt die Anf-Replikationsverbindung auf dem Volume "MyDestinationAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="4347f-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="4347f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4347f-113">PARAMETERS</span></span>

### <span data-ttu-id="4347f-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="4347f-114">-AccountName</span></span>
<span data-ttu-id="4347f-115">Der Name des ANF-Kontos des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="4347f-115">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="4347f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4347f-116">-DefaultProfile</span></span>
<span data-ttu-id="4347f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4347f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4347f-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4347f-118">-InputObject</span></span>
<span data-ttu-id="4347f-119">Das ANF-Zielvolume mit der zu entfernenden Replikation</span><span class="sxs-lookup"><span data-stu-id="4347f-119">The ANF destination volume with the replication to remove</span></span>

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

### <span data-ttu-id="4347f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4347f-120">-Name</span></span>
<span data-ttu-id="4347f-121">Der Name des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="4347f-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4347f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4347f-122">-PassThru</span></span>
<span data-ttu-id="4347f-123">Gibt zurück, ob die angegebene ANF-Replikation erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="4347f-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="4347f-124">-Poolname</span><span class="sxs-lookup"><span data-stu-id="4347f-124">-PoolName</span></span>
<span data-ttu-id="4347f-125">Der Name des ANF-Pools des Replikations Datenträgers</span><span class="sxs-lookup"><span data-stu-id="4347f-125">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="4347f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4347f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4347f-127">Die Ressourcengruppe des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="4347f-127">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4347f-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4347f-128">-ResourceId</span></span>
<span data-ttu-id="4347f-129">Die Ressourcen-ID des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="4347f-129">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4347f-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4347f-130">-Confirm</span></span>
<span data-ttu-id="4347f-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4347f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4347f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4347f-132">-WhatIf</span></span>
<span data-ttu-id="4347f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4347f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4347f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4347f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4347f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4347f-135">CommonParameters</span></span>
<span data-ttu-id="4347f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4347f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4347f-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4347f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4347f-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4347f-138">INPUTS</span></span>

### <span data-ttu-id="4347f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4347f-139">System.String</span></span>

### <span data-ttu-id="4347f-140">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="4347f-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="4347f-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4347f-141">OUTPUTS</span></span>

### <span data-ttu-id="4347f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4347f-142">System.Boolean</span></span>

## <span data-ttu-id="4347f-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="4347f-143">NOTES</span></span>

## <span data-ttu-id="4347f-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4347f-144">RELATED LINKS</span></span>
