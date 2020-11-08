---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrinmageazurev2diskinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrInMageAzureV2DiskInput.md
ms.openlocfilehash: 115287c5892a83cd38e20080cdaee8ff531a612d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004904"
---
# <span data-ttu-id="1a62e-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="1a62e-101">New-AzRecoveryServicesAsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1a62e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a62e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a62e-103">Erstellt ein Datenträger Zuordnungsobjekt für vMWare Virtual Machine-Datenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1a62e-103">Creates a disk mapping object for vMWare virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="1a62e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a62e-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId <String> -LogStorageAccountId <String>
 -DiskType <String> [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a62e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a62e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a62e-106">Erstellt ein Datenträger Zuordnungsobjekt, das einen vMWare Virtual Machine-Datenträger dem Cachespeicher Konto und dem Ziel des verwalteten Datenträgertyps (Wiederherstellungsbereich) zuordnet, der zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1a62e-106">Creates a disk mapping object that maps an vMWare virtual machine disk to the cache storage account and target managed disk type (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="1a62e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a62e-107">EXAMPLES</span></span>

### <span data-ttu-id="1a62e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a62e-108">Example 1</span></span>
```powershell
PS C:> New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
```

<span data-ttu-id="1a62e-109">Erstellen Sie ein Datenträger Zuordnungsobjekt für vMWare Virtual Machine-Datenträger, die repliziert werden sollen. Wird beim Aktivieren des Schutzes für vMWare Machine verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a62e-109">Create a disk mapping object for vMWare virtual machine disks to be replicated.Used during enable protection for vMWare machine.</span></span>

## <span data-ttu-id="1a62e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a62e-110">PARAMETERS</span></span>

### <span data-ttu-id="1a62e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a62e-111">-DefaultProfile</span></span>
<span data-ttu-id="1a62e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a62e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a62e-113">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1a62e-113">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1a62e-114">Gibt die Ressourcen-ID des Datenträger Verschlüsselungs Satzes an, der für die Verschlüsselung der verwalteten Datenträger verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a62e-114">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

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

### <span data-ttu-id="1a62e-115">-Datenträger-Nr</span><span class="sxs-lookup"><span data-stu-id="1a62e-115">-DiskId</span></span>
<span data-ttu-id="1a62e-116">Geben Sie die Datenträger-Nr des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a62e-116">Specify the DiskId of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="1a62e-117">-Disktype</span><span class="sxs-lookup"><span data-stu-id="1a62e-117">-DiskType</span></span>
<span data-ttu-id="1a62e-118">Gibt den Wiederherstellungsdaten Trägertyp an.</span><span class="sxs-lookup"><span data-stu-id="1a62e-118">Specifies the Recovery disk type.</span></span>

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

### <span data-ttu-id="1a62e-119">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1a62e-119">-LogStorageAccountId</span></span>
<span data-ttu-id="1a62e-120">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a62e-120">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="1a62e-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a62e-121">-Confirm</span></span>
<span data-ttu-id="1a62e-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a62e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a62e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a62e-123">-WhatIf</span></span>
<span data-ttu-id="1a62e-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a62e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a62e-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a62e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a62e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a62e-126">CommonParameters</span></span>
<span data-ttu-id="1a62e-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a62e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a62e-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a62e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a62e-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a62e-129">INPUTS</span></span>

### <span data-ttu-id="1a62e-130">Keine</span><span class="sxs-lookup"><span data-stu-id="1a62e-130">None</span></span>

## <span data-ttu-id="1a62e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a62e-131">OUTPUTS</span></span>

### <span data-ttu-id="1a62e-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. AsrInMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="1a62e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput</span></span>

## <span data-ttu-id="1a62e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a62e-133">NOTES</span></span>

## <span data-ttu-id="1a62e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a62e-134">RELATED LINKS</span></span>
