---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 538fe4fe21394c817b7bb2a954fbdbcc2ccfb097
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003731"
---
# <span data-ttu-id="442a8-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="442a8-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="442a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="442a8-102">SYNOPSIS</span></span>
<span data-ttu-id="442a8-103">Legt die Eigenschaften für die Sicherungsverwaltung fest.</span><span class="sxs-lookup"><span data-stu-id="442a8-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="442a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="442a8-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="442a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="442a8-105">DESCRIPTION</span></span>
<span data-ttu-id="442a8-106">Das Cmdlet " **Set-AzRecoveryServicesBackupProperty** " legt die Eigenschaften des Sicherungsspeichers für einen Vault für Wiederherstellungsdienste fest.</span><span class="sxs-lookup"><span data-stu-id="442a8-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="442a8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="442a8-107">EXAMPLES</span></span>

### <span data-ttu-id="442a8-108">Beispiel 1: Einrichten des georedundanten Speichers für einen Tresor</span><span class="sxs-lookup"><span data-stu-id="442a8-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="442a8-109">Der erste Befehl ruft den Tresor mit dem Namen TestVault ab und speichert ihn dann in der Variablen $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="442a8-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="442a8-110">Der zweite Befehl legt die Redundanz für den Sicherungsspeicher für $Vault 01 auf georedundant fest.</span><span class="sxs-lookup"><span data-stu-id="442a8-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="442a8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="442a8-111">PARAMETERS</span></span>

### <span data-ttu-id="442a8-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="442a8-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="442a8-113">Gibt den Typ der Sicherungsspeicher Redundanz an.</span><span class="sxs-lookup"><span data-stu-id="442a8-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="442a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="442a8-114">-DefaultProfile</span></span>
<span data-ttu-id="442a8-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="442a8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="442a8-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="442a8-116">-Vault</span></span>
<span data-ttu-id="442a8-117">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="442a8-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="442a8-118">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="442a8-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="442a8-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="442a8-119">-Confirm</span></span>
<span data-ttu-id="442a8-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="442a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="442a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="442a8-121">-WhatIf</span></span>
<span data-ttu-id="442a8-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="442a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="442a8-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="442a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="442a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="442a8-124">CommonParameters</span></span>
<span data-ttu-id="442a8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="442a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="442a8-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="442a8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="442a8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="442a8-127">INPUTS</span></span>

### <span data-ttu-id="442a8-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="442a8-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="442a8-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="442a8-129">OUTPUTS</span></span>

### <span data-ttu-id="442a8-130">System. void</span><span class="sxs-lookup"><span data-stu-id="442a8-130">System.Void</span></span>

## <span data-ttu-id="442a8-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="442a8-131">NOTES</span></span>

## <span data-ttu-id="442a8-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="442a8-132">RELATED LINKS</span></span>

[<span data-ttu-id="442a8-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="442a8-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="442a8-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="442a8-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


