---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: b742c8af0e8c36d07b2c608e74f0a02349502104
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660976"
---
# <span data-ttu-id="21f1b-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="21f1b-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="21f1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="21f1b-103">Erstellt ein neues Azure NetApp-Dateien (ANF)-Volume.</span><span class="sxs-lookup"><span data-stu-id="21f1b-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="21f1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21f1b-104">SYNTAX</span></span>

### <span data-ttu-id="21f1b-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="21f1b-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> -ServiceLevel <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21f1b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21f1b-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21f1b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21f1b-107">DESCRIPTION</span></span>
<span data-ttu-id="21f1b-108">Das Cmdlet **New-AzNetAppFilesVolume** erstellt ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="21f1b-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="21f1b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21f1b-109">EXAMPLES</span></span>

### <span data-ttu-id="21f1b-110">Beispiel 1: Erstellen eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21f1b-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="21f1b-111">Dieser Befehl erstellt das neue ANF-Volumen "MyAnfVolume" innerhalb des Pools "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="21f1b-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="21f1b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="21f1b-112">PARAMETERS</span></span>

### <span data-ttu-id="21f1b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="21f1b-113">-AccountName</span></span>
<span data-ttu-id="21f1b-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="21f1b-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="21f1b-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="21f1b-115">-CreationToken</span></span>
<span data-ttu-id="21f1b-116">Ein eindeutiger Dateipfad für das Volume</span><span class="sxs-lookup"><span data-stu-id="21f1b-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="21f1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21f1b-117">-DefaultProfile</span></span>
<span data-ttu-id="21f1b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21f1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21f1b-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="21f1b-119">-Location</span></span>
<span data-ttu-id="21f1b-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="21f1b-120">The location of the resource</span></span>

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

### <span data-ttu-id="21f1b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="21f1b-121">-Name</span></span>
<span data-ttu-id="21f1b-122">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21f1b-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="21f1b-123">-Poolname</span><span class="sxs-lookup"><span data-stu-id="21f1b-123">-PoolName</span></span>
<span data-ttu-id="21f1b-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="21f1b-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="21f1b-125">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="21f1b-125">-PoolObject</span></span>
<span data-ttu-id="21f1b-126">Der Pool für das neue Volumen Objekt</span><span class="sxs-lookup"><span data-stu-id="21f1b-126">The pool for the new volume object</span></span>

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

### <span data-ttu-id="21f1b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21f1b-127">-ResourceGroupName</span></span>
<span data-ttu-id="21f1b-128">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="21f1b-128">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="21f1b-129">-Service Level</span><span class="sxs-lookup"><span data-stu-id="21f1b-129">-ServiceLevel</span></span>
<span data-ttu-id="21f1b-130">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="21f1b-130">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="21f1b-131">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="21f1b-131">-SubnetId</span></span>
<span data-ttu-id="21f1b-132">Der Azure-Ressourcen-URI für ein delegiertes Subnetz</span><span class="sxs-lookup"><span data-stu-id="21f1b-132">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="21f1b-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="21f1b-133">-Tag</span></span>
<span data-ttu-id="21f1b-134">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="21f1b-134">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="21f1b-135">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="21f1b-135">-UsageThreshold</span></span>
<span data-ttu-id="21f1b-136">Das maximal zulässige Speicherkontingent für ein Dateisystem in Byte</span><span class="sxs-lookup"><span data-stu-id="21f1b-136">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="21f1b-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="21f1b-137">-Confirm</span></span>
<span data-ttu-id="21f1b-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21f1b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21f1b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21f1b-139">-WhatIf</span></span>
<span data-ttu-id="21f1b-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21f1b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21f1b-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21f1b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21f1b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21f1b-142">CommonParameters</span></span>
<span data-ttu-id="21f1b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21f1b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="21f1b-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21f1b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21f1b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21f1b-145">INPUTS</span></span>

### <span data-ttu-id="21f1b-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="21f1b-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="21f1b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21f1b-147">OUTPUTS</span></span>

### <span data-ttu-id="21f1b-148">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="21f1b-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="21f1b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="21f1b-149">NOTES</span></span>

## <span data-ttu-id="21f1b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21f1b-150">RELATED LINKS</span></span>
