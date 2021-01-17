---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362646"
---
# <span data-ttu-id="2cce0-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="2cce0-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="2cce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cce0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cce0-103">Erstellt ein Datenträgerzuordnungsobjekt für virtuelle vMWare-Computerdatenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2cce0-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="2cce0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2cce0-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cce0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cce0-105">DESCRIPTION</span></span>
<span data-ttu-id="2cce0-106">Erstellt ein Datenträgerzuordnungsobjekt, das einen virtuellen vMWare-Computerdatenträger dem Cachespeicherkonto und dem Ziel verwalteten Datenträgertyp (Wiederherstellungsregion) zuzuordnen, um den Datenträger zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="2cce0-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="2cce0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2cce0-107">EXAMPLES</span></span>

### <span data-ttu-id="2cce0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2cce0-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="2cce0-109">Erstellen Sie ein Datenträgerzuordnungsobjekt für vMWare-virtuelle Computerdatenträger, die repliziert werden sollen. Wird beim Aktivieren des Schutzes für vMWare-Computer verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cce0-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="2cce0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cce0-110">PARAMETERS</span></span>

### <span data-ttu-id="2cce0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cce0-111">-DefaultProfile</span></span>
<span data-ttu-id="2cce0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2cce0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cce0-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="2cce0-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="2cce0-114">Gibt die Ressourcen-ID des Datenträgerverschlüsselungssets an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cce0-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="2cce0-115">-DiskId</span><span class="sxs-lookup"><span data-stu-id="2cce0-115">-DiskId</span></span>
<span data-ttu-id="2cce0-116">Geben Sie die DiskId des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="2cce0-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="2cce0-117">-DiskType</span><span class="sxs-lookup"><span data-stu-id="2cce0-117">-DiskType</span></span>
<span data-ttu-id="2cce0-118">Gibt den Wiederherstellungsdatenträgertyp an.</span><span class="sxs-lookup"><span data-stu-id="2cce0-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="2cce0-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2cce0-119">-LogStorageAccountId</span></span>
<span data-ttu-id="2cce0-120">Gibt die Protokoll- oder Cachespeicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cce0-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="2cce0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cce0-121">-Confirm</span></span>
<span data-ttu-id="2cce0-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cce0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cce0-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2cce0-123">-WhatIf</span></span>
<span data-ttu-id="2cce0-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cce0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cce0-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cce0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cce0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cce0-126">CommonParameters</span></span>
<span data-ttu-id="2cce0-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cce0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cce0-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2cce0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cce0-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2cce0-129">INPUTS</span></span>

### <span data-ttu-id="2cce0-130">Keine</span><span class="sxs-lookup"><span data-stu-id="2cce0-130">None</span></span>

## <span data-ttu-id="2cce0-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2cce0-131">OUTPUTS</span></span>

### <span data-ttu-id="2cce0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="2cce0-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="2cce0-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2cce0-133">NOTES</span></span>

## <span data-ttu-id="2cce0-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2cce0-134">RELATED LINKS</span></span>
