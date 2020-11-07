---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: cad30d489b53ccfd9f45cbc619ce4384cc904903
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822035"
---
# <span data-ttu-id="21e28-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="21e28-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="21e28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21e28-102">SYNOPSIS</span></span>
<span data-ttu-id="21e28-103">Erstellt ein neues Azure NetApp-Dateien (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="21e28-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="21e28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21e28-104">SYNTAX</span></span>

### <span data-ttu-id="21e28-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21e28-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e28-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21e28-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ProtocolType <System.String[]>]
 [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e28-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21e28-107">DESCRIPTION</span></span>
<span data-ttu-id="21e28-108">Das Cmdlet **New-AzNetAppFilesVolume** erstellt ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="21e28-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="21e28-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21e28-109">EXAMPLES</span></span>

### <span data-ttu-id="21e28-110">Beispiel 1: Erstellen eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21e28-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="21e28-111">Dieser Befehl erstellt das neue ANF-Volumen "MyAnfVolume" innerhalb des Pools "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="21e28-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="21e28-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="21e28-112">PARAMETERS</span></span>

### <span data-ttu-id="21e28-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="21e28-113">-AccountName</span></span>
<span data-ttu-id="21e28-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="21e28-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="21e28-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="21e28-115">-CreationToken</span></span>
<span data-ttu-id="21e28-116">Ein eindeutiger Dateipfad für das Volume</span><span class="sxs-lookup"><span data-stu-id="21e28-116">A unique file path for the volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e28-117">-DefaultProfile</span></span>
<span data-ttu-id="21e28-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21e28-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21e28-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="21e28-119">-ExportPolicy</span></span>
<span data-ttu-id="21e28-120">Ein Hashtable-Array, das die Export Richtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="21e28-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="21e28-121">-Location</span></span>
<span data-ttu-id="21e28-122">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="21e28-122">The location of the resource</span></span>

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

### <span data-ttu-id="21e28-123">-Name</span><span class="sxs-lookup"><span data-stu-id="21e28-123">-Name</span></span>
<span data-ttu-id="21e28-124">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21e28-124">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="21e28-125">-PoolName</span></span>
<span data-ttu-id="21e28-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="21e28-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="21e28-127">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="21e28-127">-PoolObject</span></span>
<span data-ttu-id="21e28-128">Der Pool für das neue Volumen Objekt</span><span class="sxs-lookup"><span data-stu-id="21e28-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="21e28-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="21e28-129">-ProtocolType</span></span>
<span data-ttu-id="21e28-130">Ein Hashtable-Array, das die Export Richtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="21e28-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="21e28-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e28-131">-ResourceGroupName</span></span>
<span data-ttu-id="21e28-132">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="21e28-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="21e28-133">-Service Level</span><span class="sxs-lookup"><span data-stu-id="21e28-133">-ServiceLevel</span></span>
<span data-ttu-id="21e28-134">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21e28-134">The service level of the ANF volume</span></span>

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

```yaml
Type: String
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-135">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="21e28-135">-SubnetId</span></span>
<span data-ttu-id="21e28-136">Der Azure-Ressourcen-URI für ein delegiertes Subnetz</span><span class="sxs-lookup"><span data-stu-id="21e28-136">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="21e28-137">-Tag</span></span>
<span data-ttu-id="21e28-138">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="21e28-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="21e28-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="21e28-139">-UsageThreshold</span></span>
<span data-ttu-id="21e28-140">Das maximal zulässige Speicherkontingent für ein Dateisystem in Byte</span><span class="sxs-lookup"><span data-stu-id="21e28-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e28-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21e28-141">-Confirm</span></span>
<span data-ttu-id="21e28-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21e28-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e28-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e28-143">-WhatIf</span></span>
<span data-ttu-id="21e28-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21e28-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21e28-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21e28-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e28-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e28-146">CommonParameters</span></span>
<span data-ttu-id="21e28-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e28-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21e28-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e28-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e28-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21e28-149">INPUTS</span></span>

### <span data-ttu-id="21e28-150">System. String</span><span class="sxs-lookup"><span data-stu-id="21e28-150">System.String</span></span>

### <span data-ttu-id="21e28-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="21e28-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="21e28-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21e28-152">OUTPUTS</span></span>

### <span data-ttu-id="21e28-153">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="21e28-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="21e28-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="21e28-154">NOTES</span></span>

## <span data-ttu-id="21e28-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21e28-155">RELATED LINKS</span></span>
