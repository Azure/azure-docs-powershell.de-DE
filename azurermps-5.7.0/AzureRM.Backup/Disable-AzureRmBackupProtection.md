---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: cd3f5520b688d5a83cae20216fac47e9120b4cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663790"
---
# <span data-ttu-id="46e93-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="46e93-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="46e93-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46e93-102">SYNOPSIS</span></span>
<span data-ttu-id="46e93-103">Deaktiviert den Schutz für ein geschütztes Backup-Element.</span><span class="sxs-lookup"><span data-stu-id="46e93-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46e93-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46e93-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e93-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46e93-105">DESCRIPTION</span></span>
<span data-ttu-id="46e93-106">Das Cmdlet **Disable-AzureRmBackupProtection** deaktiviert den Schutz für ein Azure Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="46e93-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="46e93-107">Dieses Cmdlet beendet die reguläre geplante Sicherung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="46e93-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="46e93-108">Mit diesem Cmdlet können vorhandene Wiederherstellungspunkte für das Sicherungselement gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="46e93-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="46e93-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46e93-109">EXAMPLES</span></span>

## <span data-ttu-id="46e93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="46e93-110">PARAMETERS</span></span>

### <span data-ttu-id="46e93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e93-111">-DefaultProfile</span></span>
<span data-ttu-id="46e93-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46e93-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46e93-113">-Force</span><span class="sxs-lookup"><span data-stu-id="46e93-113">-Force</span></span>
<span data-ttu-id="46e93-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="46e93-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e93-115">-Item</span><span class="sxs-lookup"><span data-stu-id="46e93-115">-Item</span></span>
<span data-ttu-id="46e93-116">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="46e93-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="46e93-117">Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46e93-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46e93-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="46e93-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="46e93-119">Gibt an, dass dieses Cmdlet vorhandene Wiederherstellungspunkte löscht.</span><span class="sxs-lookup"><span data-stu-id="46e93-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="46e93-120">Um gespeicherte Wiederherstellungspunkte zu einem späteren Zeitpunkt zu löschen, führen Sie dieses Cmdlet erneut aus, und geben Sie diesen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="46e93-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e93-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="46e93-121">-Confirm</span></span>
<span data-ttu-id="46e93-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="46e93-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e93-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e93-123">-WhatIf</span></span>
<span data-ttu-id="46e93-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="46e93-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e93-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="46e93-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e93-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e93-126">CommonParameters</span></span>
<span data-ttu-id="46e93-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46e93-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e93-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e93-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e93-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46e93-129">INPUTS</span></span>

### <span data-ttu-id="46e93-130">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="46e93-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="46e93-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46e93-131">OUTPUTS</span></span>

### <span data-ttu-id="46e93-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="46e93-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="46e93-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="46e93-133">NOTES</span></span>

## <span data-ttu-id="46e93-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46e93-134">RELATED LINKS</span></span>

[<span data-ttu-id="46e93-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="46e93-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="46e93-136">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="46e93-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


