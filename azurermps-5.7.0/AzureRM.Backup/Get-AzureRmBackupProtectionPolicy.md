---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: d0f0e52db76f4f16f41d1758b7e568ee17d6eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481349"
---
# <span data-ttu-id="a0dc3-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0dc3-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="a0dc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="a0dc3-103">Ruft Sicherungsrichtlinien für einen sicherungstresor ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0dc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0dc3-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0dc3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="a0dc3-106">Das Cmdlet " **Get-AzureRmBackupProtectionPolicy** " ruft Sicherungsrichtlinien für einen Azure Backup Vault ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="a0dc3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="a0dc3-108">Beispiel 1: Anzeigen der Richtlinien in einem Tresor</span><span class="sxs-lookup"><span data-stu-id="a0dc3-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="a0dc3-109">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="a0dc3-110">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="a0dc3-111">Der zweite Befehl ruft alle Sicherungsschutz Richtlinien für den Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="a0dc3-112">Beispiel 2: Abrufen einer bestimmten Richtlinie aus einem Tresor</span><span class="sxs-lookup"><span data-stu-id="a0dc3-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="a0dc3-113">Der erste Befehl ruft den Tresor mit dem Namen Vault03 mit dem Cmdlet **Get-AzureRmBackupVault** ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="a0dc3-114">Der Befehl speichert das Objekt in der $Vault Variablen.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="a0dc3-115">Der zweite Befehl ruft die Sicherungsschutz Richtlinie mit dem Namen DefaultPolicy für den Tresor in $Vault ab.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="a0dc3-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0dc3-116">PARAMETERS</span></span>

### <span data-ttu-id="a0dc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0dc3-117">-DefaultProfile</span></span>
<span data-ttu-id="a0dc3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0dc3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0dc3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a0dc3-119">-Name</span></span>
<span data-ttu-id="a0dc3-120">Gibt den Namen der Richtlinie an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-120">Specifies the name of the policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0dc3-121">-Vault</span><span class="sxs-lookup"><span data-stu-id="a0dc3-121">-Vault</span></span>
<span data-ttu-id="a0dc3-122">Gibt den sicherungstresor an, für den dieses Cmdlet Richtlinien erhält.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="a0dc3-123">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0dc3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0dc3-124">CommonParameters</span></span>
<span data-ttu-id="a0dc3-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0dc3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0dc3-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0dc3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0dc3-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0dc3-127">INPUTS</span></span>

### <span data-ttu-id="a0dc3-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a0dc3-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="a0dc3-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0dc3-129">OUTPUTS</span></span>

### <span data-ttu-id="a0dc3-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0dc3-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="a0dc3-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0dc3-131">NOTES</span></span>
* <span data-ttu-id="a0dc3-132">Keine</span><span class="sxs-lookup"><span data-stu-id="a0dc3-132">None</span></span>

## <span data-ttu-id="a0dc3-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0dc3-133">RELATED LINKS</span></span>

[<span data-ttu-id="a0dc3-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a0dc3-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="a0dc3-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="a0dc3-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="a0dc3-136">Neu – AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0dc3-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="a0dc3-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a0dc3-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


