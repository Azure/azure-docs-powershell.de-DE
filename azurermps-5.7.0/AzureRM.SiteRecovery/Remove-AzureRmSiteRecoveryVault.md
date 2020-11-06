---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 63E9894A-3AC5-4397-9B21-D0A72EBA5C4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 70d0876be32b80d314dfb7a464d0626b7c534fea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476562"
---
# <span data-ttu-id="b9c82-101">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b9c82-101">Remove-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="b9c82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9c82-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c82-103">Entfernt einen Standort Wiederherstellungs Tresor.</span><span class="sxs-lookup"><span data-stu-id="b9c82-103">Removes a Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9c82-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryVault -Vault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9c82-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c82-106">Das Cmdlet **Remove-AzureRmSiteRecoveryVault** löscht ein Azure Site Recovery Vault.</span><span class="sxs-lookup"><span data-stu-id="b9c82-106">The **Remove-AzureRmSiteRecoveryVault** cmdlet deletes an Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b9c82-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9c82-107">EXAMPLES</span></span>

## <span data-ttu-id="b9c82-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9c82-108">PARAMETERS</span></span>

### <span data-ttu-id="b9c82-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c82-109">-DefaultProfile</span></span>
<span data-ttu-id="b9c82-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9c82-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c82-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="b9c82-111">-Vault</span></span>
<span data-ttu-id="b9c82-112">Gibt das Vault-Objekt der Standortwiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="b9c82-112">Specifies the Site Recovery vault object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c82-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c82-113">CommonParameters</span></span>
<span data-ttu-id="b9c82-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c82-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c82-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c82-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c82-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9c82-116">INPUTS</span></span>

### <span data-ttu-id="b9c82-117">ASRVault</span><span class="sxs-lookup"><span data-stu-id="b9c82-117">ASRVault</span></span>
<span data-ttu-id="b9c82-118">Der Parameter "Vault" akzeptiert den Wert vom Typ "ASRVault" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b9c82-118">Parameter 'Vault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="b9c82-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9c82-119">OUTPUTS</span></span>

## <span data-ttu-id="b9c82-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9c82-120">NOTES</span></span>

## <span data-ttu-id="b9c82-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9c82-121">RELATED LINKS</span></span>

[<span data-ttu-id="b9c82-122">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b9c82-122">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="b9c82-123">Neu – AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="b9c82-123">New-AzureRmSiteRecoveryVault</span></span>](./New-AzureRmSiteRecoveryVault.md)
