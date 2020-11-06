---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 2605B232-10CA-4426-9917-7C9719C15166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupcontainerreregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupContainerReregistration.md
ms.openlocfilehash: 6ae660eae9e597d92e162529ff244431d4720418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480586"
---
# <span data-ttu-id="e6bba-101">Enable-AzureRmBackupContainerReregistration</span><span class="sxs-lookup"><span data-stu-id="e6bba-101">Enable-AzureRmBackupContainerReregistration</span></span>

## <span data-ttu-id="e6bba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e6bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bba-103">Registrieren Sie einen Server erneut, um eine Verbindung mit einem sicherungstresor herzustellen.</span><span class="sxs-lookup"><span data-stu-id="e6bba-103">Reregisters a server to connect to a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6bba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6bba-104">SYNTAX</span></span>

```
Enable-AzureRmBackupContainerReregistration [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6bba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6bba-105">DESCRIPTION</span></span>
<span data-ttu-id="e6bba-106">Mit dem Cmdlet **enable-AzureRmBackupContainerReregistration** wird ein Server erneut registriert, um eine Verbindung mit einem Azure Backup Vault herzustellen und die Backup-Wiederherstellungspunkt Kette fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="e6bba-106">The **Enable-AzureRmBackupContainerReregistration** cmdlet reregisters a server to connect to an Azure Backup vault and continue the Backup recovery point chain.</span></span>
<span data-ttu-id="e6bba-107">Wenn Sie einen Server zerstören, verbleiben alle seine Cloud-Sicherungspunkte im Sicherungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e6bba-107">If you destroy a server, all its cloud backup points remain in the Backup vault.</span></span>
<span data-ttu-id="e6bba-108">Wenn Sie einen Ersatzserver erstellen und ihm denselben vollqualifizierten Domänennamen zuweisen, können Sie den Server wieder mit demselben Tresor verbinden.</span><span class="sxs-lookup"><span data-stu-id="e6bba-108">If you create a replacement server and assign it the same fully qualified domain name, you can connect the server back to the same vault.</span></span>
<span data-ttu-id="e6bba-109">Mit diesem Cmdlet kann die Sicherung Backups erstellen und dem vorhandenen Satz neue Sicherungspunkte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e6bba-109">This cmdlet enables Backup to make backups and add new backup points to the existing set.</span></span>
<span data-ttu-id="e6bba-110">Das neue, das der Server in der Sicherungskette fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="e6bba-110">The new the server continues in the backup chain.</span></span>

## <span data-ttu-id="e6bba-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e6bba-111">EXAMPLES</span></span>

## <span data-ttu-id="e6bba-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6bba-112">PARAMETERS</span></span>

### <span data-ttu-id="e6bba-113">-Container</span><span class="sxs-lookup"><span data-stu-id="e6bba-113">-Container</span></span>
<span data-ttu-id="e6bba-114">Gibt den Container an, der von diesem Cmdlet erneut registriert wird.</span><span class="sxs-lookup"><span data-stu-id="e6bba-114">Specifies the container that this cmdlet reregisters.</span></span>
<span data-ttu-id="e6bba-115">Verwenden Sie zum Abrufen eines **AzureRmBackupContainer** das Get-AzureRmBackupContainer-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6bba-115">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bba-116">-DefaultProfile</span></span>
<span data-ttu-id="e6bba-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e6bba-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6bba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bba-118">CommonParameters</span></span>
<span data-ttu-id="e6bba-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6bba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bba-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6bba-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bba-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e6bba-121">INPUTS</span></span>

### <span data-ttu-id="e6bba-122">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e6bba-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="e6bba-123">Parameter: Container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6bba-123">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="e6bba-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e6bba-124">OUTPUTS</span></span>

### <span data-ttu-id="e6bba-125">System. void</span><span class="sxs-lookup"><span data-stu-id="e6bba-125">System.Void</span></span>

## <span data-ttu-id="e6bba-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e6bba-126">NOTES</span></span>

## <span data-ttu-id="e6bba-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e6bba-127">RELATED LINKS</span></span>

[<span data-ttu-id="e6bba-128">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e6bba-128">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="e6bba-129">Registrieren-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="e6bba-129">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


