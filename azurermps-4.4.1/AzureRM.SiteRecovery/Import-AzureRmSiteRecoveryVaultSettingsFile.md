---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 070DA86E-9EA4-4777-9D53-64B58B4401B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Import-AzureRmSiteRecoveryVaultSettingsFile.md
ms.openlocfilehash: 42863e0dbf6982ced1f77f916c97ed4fc19d6979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503937"
---
# <span data-ttu-id="6870e-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6870e-101">Import-AzureRmSiteRecoveryVaultSettingsFile</span></span>

## <span data-ttu-id="6870e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6870e-102">SYNOPSIS</span></span>
<span data-ttu-id="6870e-103">Importiert eine Vault-Einstellungsdatei für eine Websitewiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="6870e-103">Imports a Site Recovery vault settings file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6870e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6870e-104">SYNTAX</span></span>

```
Import-AzureRmSiteRecoveryVaultSettingsFile [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6870e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6870e-105">DESCRIPTION</span></span>
<span data-ttu-id="6870e-106">Das Cmdlet " **Import-AzureRmSiteRecoveryVaultSettingsFile** " importiert eine Azure Site Recovery Vault Settings-Datei, um den Vault-Kontext für nachfolgende Website Wiederherstellungsvorgänge in der aktuellen Sitzung einzurichten.</span><span class="sxs-lookup"><span data-stu-id="6870e-106">The **Import-AzureRmSiteRecoveryVaultSettingsFile** cmdlet imports an Azure Site Recovery vault settings file to set the vault context for subsequent Site Recovery operations in the current session.</span></span>

## <span data-ttu-id="6870e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6870e-107">EXAMPLES</span></span>

## <span data-ttu-id="6870e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6870e-108">PARAMETERS</span></span>

### <span data-ttu-id="6870e-109">-Path</span><span class="sxs-lookup"><span data-stu-id="6870e-109">-Path</span></span>
<span data-ttu-id="6870e-110">Gibt den Pfad der Datei für die Vault-Einstellungen der Websitewiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="6870e-110">Specifies the path of the Site Recovery vault settings file.</span></span>
<span data-ttu-id="6870e-111">Diese Datei kann aus dem Vault-Portal der Websitewiederherstellung heruntergeladen und lokal gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="6870e-111">This file can be downloaded from the Site Recovery vault portal and stored locally.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6870e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6870e-112">-DefaultProfile</span></span>
<span data-ttu-id="6870e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6870e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6870e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6870e-114">CommonParameters</span></span>
<span data-ttu-id="6870e-115">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6870e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6870e-116">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6870e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6870e-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6870e-117">INPUTS</span></span>

## <span data-ttu-id="6870e-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6870e-118">OUTPUTS</span></span>

### <span data-ttu-id="6870e-119">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="6870e-119">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="6870e-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="6870e-120">NOTES</span></span>

## <span data-ttu-id="6870e-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6870e-121">RELATED LINKS</span></span>

[<span data-ttu-id="6870e-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="6870e-122">Get-AzureRmSiteRecoveryVaultSettingsFile</span></span>](./Get-AzureRmSiteRecoveryVaultSettingsFile.md)
