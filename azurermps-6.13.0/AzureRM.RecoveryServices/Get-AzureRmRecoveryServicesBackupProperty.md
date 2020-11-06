---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482153"
---
# <span data-ttu-id="52719-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="52719-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="52719-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52719-102">SYNOPSIS</span></span>
<span data-ttu-id="52719-103">Ruft Sicherungseigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="52719-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52719-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52719-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="52719-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52719-105">DESCRIPTION</span></span>
<span data-ttu-id="52719-106">Das Cmdlet " **Get-AzureRmRecoveryServicesBackupProperty** " ruft Sicherungseigenschaften für einen Vault für Wiederherstellungsdienste ab.</span><span class="sxs-lookup"><span data-stu-id="52719-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="52719-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52719-107">EXAMPLES</span></span>

### <span data-ttu-id="52719-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="52719-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="52719-109">Rufen Sie die Vault-Sicherungseigenschaft für Vault ab.</span><span class="sxs-lookup"><span data-stu-id="52719-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="52719-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="52719-110">PARAMETERS</span></span>

### <span data-ttu-id="52719-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="52719-111">-Vault</span></span>
<span data-ttu-id="52719-112">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="52719-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="52719-113">Der Tresor muss ein **AzureRmRecoveryServicesVault** -Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="52719-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="52719-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52719-114">-DefaultProfile</span></span>
<span data-ttu-id="52719-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52719-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52719-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52719-116">CommonParameters</span></span>
<span data-ttu-id="52719-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52719-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52719-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52719-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52719-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52719-119">INPUTS</span></span>

### <span data-ttu-id="52719-120">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="52719-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="52719-121">Parameter: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52719-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="52719-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52719-122">OUTPUTS</span></span>

### <span data-ttu-id="52719-123">Microsoft. Azure. Commands. RecoveryServices. ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="52719-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="52719-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="52719-124">NOTES</span></span>

## <span data-ttu-id="52719-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52719-125">RELATED LINKS</span></span>
