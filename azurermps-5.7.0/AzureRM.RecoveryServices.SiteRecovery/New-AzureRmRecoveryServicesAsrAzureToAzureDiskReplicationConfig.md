---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 542e75ed0e6531f5778f9793b678b42f953c15d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476685"
---
# <span data-ttu-id="d5ed4-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d5ed4-101">New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d5ed4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ed4-103">Erstellt ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5ed4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5ed4-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5ed4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5ed4-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ed4-106">Erstellt ein Datenträger Zuordnungsobjekt, das einen Azure Virtual Machine-Datenträger dem Cachespeicher Konto und dem Zielspeicher Konto (Wiederherstellungsbereich) zuordnet, das zum Replizieren des Datenträgers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-106">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="d5ed4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5ed4-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ed4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5ed4-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="d5ed4-109">Erstellen Sie ein Datenträger Zuordnungsobjekt für Azure Virtual Machine-Datenträger, die repliziert werden sollen. Wird während Azure zu Azure enabledr verwendet, und der Vorgang wird erneut geschützt.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-109">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and reprotect operation.</span></span>

## <span data-ttu-id="d5ed4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5ed4-110">PARAMETERS</span></span>

### <span data-ttu-id="d5ed4-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5ed4-111">-Confirm</span></span>
<span data-ttu-id="d5ed4-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ed4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ed4-113">-DefaultProfile</span></span>
<span data-ttu-id="d5ed4-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5ed4-115">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d5ed4-115">-LogStorageAccountId</span></span>
<span data-ttu-id="d5ed4-116">Gibt die Protokoll-oder Cache-Speicherkonto-ID an, die zum Speichern von Replikationsprotokollen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-116">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="d5ed4-117">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d5ed4-117">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d5ed4-118">Gibt die ID des Azure-speicherkontos an, in das repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-118">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="d5ed4-119">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="d5ed4-119">-VhdUri</span></span>
<span data-ttu-id="d5ed4-120">Geben Sie den VHD-URI des Datenträgers an, dem diese Zuordnung entspricht.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-120">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="d5ed4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ed4-121">-WhatIf</span></span>
<span data-ttu-id="d5ed4-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5ed4-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ed4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ed4-124">CommonParameters</span></span>
<span data-ttu-id="d5ed4-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ed4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ed4-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ed4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ed4-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5ed4-127">INPUTS</span></span>

### <span data-ttu-id="d5ed4-128">Keine</span><span class="sxs-lookup"><span data-stu-id="d5ed4-128">None</span></span>

## <span data-ttu-id="d5ed4-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5ed4-129">OUTPUTS</span></span>

### <span data-ttu-id="d5ed4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="d5ed4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzureRmRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="d5ed4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5ed4-131">NOTES</span></span>

## <span data-ttu-id="d5ed4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5ed4-132">RELATED LINKS</span></span>
