---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: b208602532428d14c2af1504c5b8af2cce0b155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479937"
---
# <span data-ttu-id="9ddd5-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="9ddd5-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="9ddd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ddd5-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddd5-103">Lädt die Vault-Anmeldeinformationsdatei für einen Sicherungsspeicher herunter.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ddd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ddd5-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ddd5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ddd5-105">DESCRIPTION</span></span>
<span data-ttu-id="9ddd5-106">Das Cmdlet " **Get-AzureRmBackupVaultCredentials** " downloadet die Vault-Anmeldeinformationsdatei für ein Azure Backup Vault.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="9ddd5-107">Bei der Sicherung wird eine Vault-Anmeldeinformationsdatei verwendet, um einen Server mit dem Azure Backup Vault zu verbinden und zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="9ddd5-108">Sie müssen einen Server registrieren, bevor Sicherungsdaten an den Tresor gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="9ddd5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ddd5-109">EXAMPLES</span></span>

## <span data-ttu-id="9ddd5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ddd5-110">PARAMETERS</span></span>

### <span data-ttu-id="9ddd5-111">-Zielstandort</span><span class="sxs-lookup"><span data-stu-id="9ddd5-111">-TargetLocation</span></span>
<span data-ttu-id="9ddd5-112">Gibt den Zielpfad an, in dem dieses Cmdlet die Vault-Anmeldeinformationsdatei speichert.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-112">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd5-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="9ddd5-113">-Vault</span></span>
<span data-ttu-id="9ddd5-114">Gibt den sicherungstresor an, für den dieses Cmdlet eine Vault-Anmeldeinformationsdatei erhält.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-114">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="9ddd5-115">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-115">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddd5-116">-DefaultProfile</span></span>
<span data-ttu-id="9ddd5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ddd5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddd5-118">CommonParameters</span></span>
<span data-ttu-id="9ddd5-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddd5-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ddd5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddd5-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ddd5-121">INPUTS</span></span>

### <span data-ttu-id="9ddd5-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="9ddd5-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="9ddd5-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ddd5-123">OUTPUTS</span></span>

### <span data-ttu-id="9ddd5-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="9ddd5-124">String</span></span>
<span data-ttu-id="9ddd5-125">Dieses Cmdlet gibt den Namen der Vault-Anmeldeinformationsdatei zurück.</span><span class="sxs-lookup"><span data-stu-id="9ddd5-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="9ddd5-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ddd5-126">NOTES</span></span>

## <span data-ttu-id="9ddd5-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ddd5-127">RELATED LINKS</span></span>

[<span data-ttu-id="9ddd5-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9ddd5-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


