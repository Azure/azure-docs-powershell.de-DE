---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660964"
---
# <span data-ttu-id="b4257-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4257-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="b4257-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4257-102">SYNOPSIS</span></span>
<span data-ttu-id="b4257-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Volume entsprechend den bereitgestellten optionalen Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="b4257-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="b4257-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4257-104">SYNTAX</span></span>

### <span data-ttu-id="b4257-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4257-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4257-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4257-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4257-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4257-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4257-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4257-108">DESCRIPTION</span></span>
<span data-ttu-id="b4257-109">Das Cmdlet **Update-AzNetAppFilesVolume** aktualisiert ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="b4257-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="b4257-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4257-110">EXAMPLES</span></span>

### <span data-ttu-id="b4257-111">Beispiel 1: Aktualisieren eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="b4257-111">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="b4257-112">Mit diesem Befehl wird das ANF-Volumen "MyAnfVolume" mit der neuen UsageThreshold-Größe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b4257-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="b4257-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4257-113">PARAMETERS</span></span>

### <span data-ttu-id="b4257-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="b4257-114">-AccountName</span></span>
<span data-ttu-id="b4257-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="b4257-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4257-116">-DefaultProfile</span></span>
<span data-ttu-id="b4257-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4257-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4257-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b4257-118">-InputObject</span></span>
<span data-ttu-id="b4257-119">Das zu aktualisierbare Volume-Objekt</span><span class="sxs-lookup"><span data-stu-id="b4257-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="b4257-120">-Location</span></span>
<span data-ttu-id="b4257-121">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="b4257-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b4257-122">-Name</span></span>
<span data-ttu-id="b4257-123">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="b4257-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-124">-Poolname</span><span class="sxs-lookup"><span data-stu-id="b4257-124">-PoolName</span></span>
<span data-ttu-id="b4257-125">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="b4257-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-126">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="b4257-126">-PoolObject</span></span>
<span data-ttu-id="b4257-127">Das Pool-Objekt, das das zu aktualisierbare Volume enthält</span><span class="sxs-lookup"><span data-stu-id="b4257-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4257-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4257-129">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="b4257-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-130">-Service Level</span><span class="sxs-lookup"><span data-stu-id="b4257-130">-ServiceLevel</span></span>
<span data-ttu-id="b4257-131">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="b4257-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4257-132">-Tag</span></span>
<span data-ttu-id="b4257-133">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="b4257-133">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="b4257-134">-UsageThreshold</span></span>
<span data-ttu-id="b4257-135">Das maximal zulässige Speicherkontingent für ein Dateisystem in Byte</span><span class="sxs-lookup"><span data-stu-id="b4257-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4257-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4257-136">-Confirm</span></span>
<span data-ttu-id="b4257-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4257-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4257-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4257-138">-WhatIf</span></span>
<span data-ttu-id="b4257-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4257-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4257-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4257-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4257-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4257-141">CommonParameters</span></span>
<span data-ttu-id="b4257-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4257-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b4257-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4257-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4257-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4257-144">INPUTS</span></span>

### <span data-ttu-id="b4257-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="b4257-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="b4257-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4257-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b4257-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4257-147">OUTPUTS</span></span>

### <span data-ttu-id="b4257-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="b4257-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="b4257-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4257-149">NOTES</span></span>

## <span data-ttu-id="b4257-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4257-150">RELATED LINKS</span></span>
