---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 410cd159aacadd83ee03c6e628339be38ca42d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824339"
---
# <span data-ttu-id="19557-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="19557-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="19557-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19557-102">SYNOPSIS</span></span>
<span data-ttu-id="19557-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="19557-103">Gets Backup properties.</span></span>

## <span data-ttu-id="19557-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19557-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19557-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19557-105">DESCRIPTION</span></span>
<span data-ttu-id="19557-106">Das Cmdlet " **Get-AzRecoveryServicesBackupProperty** " ruft Sicherungseigenschaften für einen Vault für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="19557-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="19557-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19557-107">EXAMPLES</span></span>

### <span data-ttu-id="19557-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="19557-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="19557-109">Rufen Sie die Vault-Sicherungseigenschaft für Vault ab.</span><span class="sxs-lookup"><span data-stu-id="19557-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="19557-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19557-110">PARAMETERS</span></span>

### <span data-ttu-id="19557-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19557-111">-DefaultProfile</span></span>
<span data-ttu-id="19557-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19557-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19557-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="19557-113">-Vault</span></span>
<span data-ttu-id="19557-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="19557-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="19557-115">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="19557-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="19557-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19557-116">CommonParameters</span></span>
<span data-ttu-id="19557-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19557-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19557-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19557-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19557-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19557-119">INPUTS</span></span>

### <span data-ttu-id="19557-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="19557-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="19557-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19557-121">OUTPUTS</span></span>

### <span data-ttu-id="19557-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="19557-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="19557-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="19557-123">NOTES</span></span>

## <span data-ttu-id="19557-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19557-124">RELATED LINKS</span></span>
