---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477753"
---
# <span data-ttu-id="49660-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="49660-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="49660-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49660-102">SYNOPSIS</span></span>
<span data-ttu-id="49660-103">Legt die Eigenschaften für die Sicherungsverwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="49660-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49660-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49660-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49660-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49660-105">DESCRIPTION</span></span>
<span data-ttu-id="49660-106">Das Cmdlet " **Set-AzureRmRecoveryServicesBackupProperties** " legt die Eigenschaften des Sicherungsspeichers für einen Vault für Wiederherstellungsdienste fest.</span><span class="sxs-lookup"><span data-stu-id="49660-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="49660-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49660-107">EXAMPLES</span></span>

### <span data-ttu-id="49660-108">Beispiel 1: Einrichten des georedundanten Speichers für einen Tresor</span><span class="sxs-lookup"><span data-stu-id="49660-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="49660-109">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="49660-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="49660-110">Der zweite Befehl legt die Redundanz für den Sicherungsspeicher für $Vault 01 auf georedundant fest.</span><span class="sxs-lookup"><span data-stu-id="49660-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="49660-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="49660-111">PARAMETERS</span></span>

### <span data-ttu-id="49660-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="49660-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="49660-113">Gibt den Typ der Sicherungsspeicher Redundanz an.</span><span class="sxs-lookup"><span data-stu-id="49660-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49660-114">-Vault</span><span class="sxs-lookup"><span data-stu-id="49660-114">-Vault</span></span>
<span data-ttu-id="49660-115">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="49660-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="49660-116">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="49660-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49660-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="49660-117">-Confirm</span></span>
<span data-ttu-id="49660-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="49660-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49660-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49660-119">-WhatIf</span></span>
<span data-ttu-id="49660-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="49660-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49660-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49660-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49660-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49660-122">-DefaultProfile</span></span>
<span data-ttu-id="49660-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49660-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49660-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49660-124">CommonParameters</span></span>
<span data-ttu-id="49660-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49660-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49660-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49660-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49660-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49660-127">INPUTS</span></span>

### <span data-ttu-id="49660-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="49660-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="49660-129">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="49660-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="49660-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49660-130">OUTPUTS</span></span>

### <span data-ttu-id="49660-131">System. void</span><span class="sxs-lookup"><span data-stu-id="49660-131">System.Void</span></span>

## <span data-ttu-id="49660-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="49660-132">NOTES</span></span>

## <span data-ttu-id="49660-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49660-133">RELATED LINKS</span></span>

[<span data-ttu-id="49660-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="49660-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="49660-135">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="49660-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


