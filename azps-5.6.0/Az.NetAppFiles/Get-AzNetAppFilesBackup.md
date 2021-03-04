---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 8a4183c148eda0f5f560d24c2b5874ff5577e85e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926931"
---
# <span data-ttu-id="3e681-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3e681-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="3e681-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e681-102">SYNOPSIS</span></span>
<span data-ttu-id="3e681-103">Ruft Details einer Azure NetApp Files (ANF)-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="3e681-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="3e681-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e681-104">SYNTAX</span></span>

### <span data-ttu-id="3e681-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e681-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e681-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e681-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e681-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e681-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e681-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e681-108">DESCRIPTION</span></span>
<span data-ttu-id="3e681-109">Das **Get-AzNetAppFilesBackup-Cmdlet** ruft Details einer ANF-Sicherung ab.</span><span class="sxs-lookup"><span data-stu-id="3e681-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="3e681-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e681-110">EXAMPLES</span></span>

### <span data-ttu-id="3e681-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3e681-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="3e681-112">Dieser Befehl ruft den Backcup mit dem Namen "MyAnfAccount" aus dem Volume mit dem Namen "MyVolume" ab.</span><span class="sxs-lookup"><span data-stu-id="3e681-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="3e681-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3e681-113">PARAMETERS</span></span>

### <span data-ttu-id="3e681-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3e681-114">-AccountName</span></span>
<span data-ttu-id="3e681-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3e681-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="3e681-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e681-116">-DefaultProfile</span></span>
<span data-ttu-id="3e681-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e681-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e681-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3e681-118">-Name</span></span>
<span data-ttu-id="3e681-119">Der Name der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="3e681-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e681-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3e681-120">-PoolName</span></span>
<span data-ttu-id="3e681-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="3e681-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="3e681-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e681-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e681-123">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="3e681-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="3e681-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e681-124">-ResourceId</span></span>
<span data-ttu-id="3e681-125">Die Ressourcen-ID der ANF-Sicherung</span><span class="sxs-lookup"><span data-stu-id="3e681-125">The resource id of the ANF Backup</span></span>

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

### <span data-ttu-id="3e681-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="3e681-126">-VolumeName</span></span>
<span data-ttu-id="3e681-127">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="3e681-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e681-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="3e681-128">-VolumeObject</span></span>
<span data-ttu-id="3e681-129">Das Volumeobjekt, das die zurückzukehrende Sicherung enthält</span><span class="sxs-lookup"><span data-stu-id="3e681-129">The volume object containing the backup to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e681-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e681-130">CommonParameters</span></span>
<span data-ttu-id="3e681-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e681-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e681-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e681-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e681-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e681-133">INPUTS</span></span>

### <span data-ttu-id="3e681-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3e681-134">System.String</span></span>

### <span data-ttu-id="3e681-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3e681-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3e681-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e681-136">OUTPUTS</span></span>

### <span data-ttu-id="3e681-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="3e681-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="3e681-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3e681-138">NOTES</span></span>

## <span data-ttu-id="3e681-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3e681-139">RELATED LINKS</span></span>
