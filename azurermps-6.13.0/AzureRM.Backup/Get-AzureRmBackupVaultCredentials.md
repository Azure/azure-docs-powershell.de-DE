---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663679"
---
# <span data-ttu-id="388f4-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="388f4-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="388f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="388f4-102">SYNOPSIS</span></span>
<span data-ttu-id="388f4-103">Lädt die Vault-Anmeldeinformationsdatei für einen Sicherungsspeicher herunter.</span><span class="sxs-lookup"><span data-stu-id="388f4-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="388f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="388f4-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="388f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="388f4-105">DESCRIPTION</span></span>
<span data-ttu-id="388f4-106">Das Cmdlet " **Get-AzureRmBackupVaultCredentials** " downloadet die Vault-Anmeldeinformationsdatei für ein Azure Backup Vault.</span><span class="sxs-lookup"><span data-stu-id="388f4-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>
<span data-ttu-id="388f4-107">Bei der Sicherung wird eine Vault-Anmeldeinformationsdatei verwendet, um einen Server mit dem Azure Backup Vault zu verbinden und zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="388f4-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="388f4-108">Sie müssen einen Server registrieren, bevor Sicherungsdaten an den Tresor gesendet werden können.</span><span class="sxs-lookup"><span data-stu-id="388f4-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="388f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="388f4-109">EXAMPLES</span></span>

## <span data-ttu-id="388f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="388f4-110">PARAMETERS</span></span>

### <span data-ttu-id="388f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="388f4-111">-DefaultProfile</span></span>
<span data-ttu-id="388f4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="388f4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="388f4-113">-Zielstandort</span><span class="sxs-lookup"><span data-stu-id="388f4-113">-TargetLocation</span></span>
<span data-ttu-id="388f4-114">Gibt den Zielpfad an, in dem dieses Cmdlet die Vault-Anmeldeinformationsdatei speichert.</span><span class="sxs-lookup"><span data-stu-id="388f4-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

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

### <span data-ttu-id="388f4-115">-Vault</span><span class="sxs-lookup"><span data-stu-id="388f4-115">-Vault</span></span>
<span data-ttu-id="388f4-116">Gibt den sicherungstresor an, für den dieses Cmdlet eine Vault-Anmeldeinformationsdatei erhält.</span><span class="sxs-lookup"><span data-stu-id="388f4-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="388f4-117">Verwenden Sie das Get-AzureRmBackupVault-Cmdlet, um ein **AzureRmBackupVault** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="388f4-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="388f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388f4-118">CommonParameters</span></span>
<span data-ttu-id="388f4-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="388f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388f4-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388f4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388f4-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="388f4-121">INPUTS</span></span>

### <span data-ttu-id="388f4-122">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="388f4-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="388f4-123">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="388f4-123">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="388f4-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="388f4-124">OUTPUTS</span></span>

### <span data-ttu-id="388f4-125">System. String</span><span class="sxs-lookup"><span data-stu-id="388f4-125">System.String</span></span>
<span data-ttu-id="388f4-126">Dieses Cmdlet gibt den Namen der Vault-Anmeldeinformationsdatei zurück.</span><span class="sxs-lookup"><span data-stu-id="388f4-126">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="388f4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="388f4-127">NOTES</span></span>

## <span data-ttu-id="388f4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="388f4-128">RELATED LINKS</span></span>

[<span data-ttu-id="388f4-129">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="388f4-129">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


