---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502246"
---
# <span data-ttu-id="e401b-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e401b-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="e401b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e401b-102">SYNOPSIS</span></span>
<span data-ttu-id="e401b-103">Deaktiviert den Schutz für ein geschütztes Backup-Element.</span><span class="sxs-lookup"><span data-stu-id="e401b-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e401b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e401b-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e401b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e401b-105">DESCRIPTION</span></span>
<span data-ttu-id="e401b-106">Das Cmdlet **Disable-AzureRmBackupProtection** deaktiviert den Schutz für ein Azure Backup-geschütztes Element.</span><span class="sxs-lookup"><span data-stu-id="e401b-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="e401b-107">Dieses Cmdlet beendet die reguläre geplante Sicherung eines Elements.</span><span class="sxs-lookup"><span data-stu-id="e401b-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="e401b-108">Mit diesem Cmdlet können vorhandene Wiederherstellungspunkte für das Sicherungselement gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e401b-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="e401b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e401b-109">EXAMPLES</span></span>

## <span data-ttu-id="e401b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e401b-110">PARAMETERS</span></span>

### <span data-ttu-id="e401b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e401b-111">-DefaultProfile</span></span>
<span data-ttu-id="e401b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e401b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e401b-113">-Force</span></span>
<span data-ttu-id="e401b-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e401b-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-115">-Item</span><span class="sxs-lookup"><span data-stu-id="e401b-115">-Item</span></span>
<span data-ttu-id="e401b-116">Gibt das Sicherungselement an, für das dieses Cmdlet den Schutz deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e401b-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="e401b-117">Verwenden Sie zum Abrufen eines **AzureRmBackupItem** das Get-AzureRmBackupItem-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e401b-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="e401b-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="e401b-119">Gibt an, dass dieses Cmdlet vorhandene Wiederherstellungspunkte löscht.</span><span class="sxs-lookup"><span data-stu-id="e401b-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="e401b-120">Um gespeicherte Wiederherstellungspunkte zu einem späteren Zeitpunkt zu löschen, führen Sie dieses Cmdlet erneut aus, und geben Sie diesen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="e401b-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e401b-121">-Confirm</span></span>
<span data-ttu-id="e401b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e401b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e401b-123">-WhatIf</span></span>
<span data-ttu-id="e401b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e401b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e401b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e401b-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e401b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e401b-126">CommonParameters</span></span>
<span data-ttu-id="e401b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e401b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e401b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e401b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e401b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e401b-129">INPUTS</span></span>

### <span data-ttu-id="e401b-130">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="e401b-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="e401b-131">Parameter: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e401b-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="e401b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e401b-132">OUTPUTS</span></span>

### <span data-ttu-id="e401b-133">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="e401b-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="e401b-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="e401b-134">NOTES</span></span>

## <span data-ttu-id="e401b-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e401b-135">RELATED LINKS</span></span>

[<span data-ttu-id="e401b-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e401b-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="e401b-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="e401b-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


