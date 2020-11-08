---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995586"
---
# <span data-ttu-id="6d17b-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="6d17b-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="6d17b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d17b-102">SYNOPSIS</span></span>
<span data-ttu-id="6d17b-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="6d17b-103">Gets Backup properties.</span></span>

## <span data-ttu-id="6d17b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d17b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d17b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d17b-105">DESCRIPTION</span></span>
<span data-ttu-id="6d17b-106">Das Cmdlet " **Get-AzRecoveryServicesBackupProperty** " ruft Sicherungseigenschaften für einen Vault für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="6d17b-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="6d17b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d17b-107">EXAMPLES</span></span>

### <span data-ttu-id="6d17b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d17b-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="6d17b-109">Rufen Sie die Vault-Sicherungseigenschaft für Vault ab.</span><span class="sxs-lookup"><span data-stu-id="6d17b-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="6d17b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d17b-110">PARAMETERS</span></span>

### <span data-ttu-id="6d17b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d17b-111">-DefaultProfile</span></span>
<span data-ttu-id="6d17b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d17b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d17b-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="6d17b-113">-Vault</span></span>
<span data-ttu-id="6d17b-114">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="6d17b-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="6d17b-115">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="6d17b-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="6d17b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d17b-116">CommonParameters</span></span>
<span data-ttu-id="6d17b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d17b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d17b-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d17b-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d17b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d17b-119">INPUTS</span></span>

### <span data-ttu-id="6d17b-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6d17b-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6d17b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d17b-121">OUTPUTS</span></span>

### <span data-ttu-id="6d17b-122">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="6d17b-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="6d17b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d17b-123">NOTES</span></span>

## <span data-ttu-id="6d17b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d17b-124">RELATED LINKS</span></span>
