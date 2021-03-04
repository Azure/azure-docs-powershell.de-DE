---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 857bc438d1c51b28e3ead1095ca4722fce7ccc8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921635"
---
# <span data-ttu-id="47a87-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="47a87-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="47a87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a87-102">SYNOPSIS</span></span>
<span data-ttu-id="47a87-103">Erstellt ein Datenträgerzuordnungsobjekt für vMWare-Virtuelle Computerlaufwerke, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47a87-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="47a87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47a87-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a87-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47a87-105">DESCRIPTION</span></span>
<span data-ttu-id="47a87-106">Erstellt ein Datenträgerzuordnungsobjekt, das einen virtuellen vMWare-Computerdatenträger dem Cachespeicherkonto und dem Ziel verwalteten Datenträgertyp (Wiederherstellungsregion) zuzuordnen, der zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47a87-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="47a87-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="47a87-107">EXAMPLES</span></span>

### <span data-ttu-id="47a87-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47a87-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="47a87-109">Erstellen Sie ein Datenträgerzuordnungsobjekt für vMWare-Virtuelle Computerlaufwerke, die repliziert werden sollen. Wird beim Aktivieren des Schutzes für vMWare-Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="47a87-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="47a87-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="47a87-110">PARAMETERS</span></span>

### <span data-ttu-id="47a87-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a87-111">-DefaultProfile</span></span>
<span data-ttu-id="47a87-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47a87-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a87-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="47a87-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="47a87-114">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssatzs an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47a87-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a87-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="47a87-115">-DiskId</span></span>
<span data-ttu-id="47a87-116">Geben Sie die DiskId des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="47a87-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a87-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="47a87-117">-DiskType</span></span>
<span data-ttu-id="47a87-118">Gibt den Wiederherstellungsdatenträgertyp an.</span><span class="sxs-lookup"><span data-stu-id="47a87-118">Specifies the Recovery disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a87-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47a87-119">-LogStorageAccountId</span></span>
<span data-ttu-id="47a87-120">Gibt die Log- oder Cachespeicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47a87-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47a87-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47a87-121">-Confirm</span></span>
<span data-ttu-id="47a87-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47a87-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a87-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a87-123">-WhatIf</span></span>
<span data-ttu-id="47a87-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47a87-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a87-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47a87-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a87-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a87-126">CommonParameters</span></span>
<span data-ttu-id="47a87-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a87-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a87-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47a87-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a87-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="47a87-129">INPUTS</span></span>

### <span data-ttu-id="47a87-130">Keine</span><span class="sxs-lookup"><span data-stu-id="47a87-130">None</span></span>

## <span data-ttu-id="47a87-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="47a87-131">OUTPUTS</span></span>

### <span data-ttu-id="47a87-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="47a87-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="47a87-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="47a87-133">NOTES</span></span>

## <span data-ttu-id="47a87-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="47a87-134">RELATED LINKS</span></span>
