---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 7F6B72A5-12F5-47EA-B5C3-E22F73377D8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryVault.md
ms.openlocfilehash: 786e3c17ca64acf908d06b88462f44af502e36c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662890"
---
# <span data-ttu-id="5fea1-101">New-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5fea1-101">New-AzureRmSiteRecoveryVault</span></span>

## <span data-ttu-id="5fea1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5fea1-102">SYNOPSIS</span></span>
<span data-ttu-id="5fea1-103">Erstellt einen Vault für Website Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="5fea1-103">Creates a Site Recovery services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fea1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5fea1-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fea1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5fea1-105">DESCRIPTION</span></span>
<span data-ttu-id="5fea1-106">Mit dem Cmdlet **New-AzureRmSiteRecoveryVault** wird ein Azure Site Recovery Services Vault erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fea1-106">The **New-AzureRmSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="5fea1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5fea1-107">EXAMPLES</span></span>

## <span data-ttu-id="5fea1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fea1-108">PARAMETERS</span></span>

### <span data-ttu-id="5fea1-109">-Standort</span><span class="sxs-lookup"><span data-stu-id="5fea1-109">-Location</span></span>
<span data-ttu-id="5fea1-110">Gibt den Namen des geografischen Standorts an.</span><span class="sxs-lookup"><span data-stu-id="5fea1-110">Specifies the geographical location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fea1-111">-Name</span><span class="sxs-lookup"><span data-stu-id="5fea1-111">-Name</span></span>
<span data-ttu-id="5fea1-112">Gibt den Namen des Tresors an.</span><span class="sxs-lookup"><span data-stu-id="5fea1-112">Specifies the name of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fea1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fea1-113">-ResourceGroupName</span></span>
<span data-ttu-id="5fea1-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5fea1-114">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fea1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fea1-115">-DefaultProfile</span></span>
<span data-ttu-id="5fea1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5fea1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fea1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fea1-117">CommonParameters</span></span>
<span data-ttu-id="5fea1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fea1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fea1-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fea1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fea1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5fea1-120">INPUTS</span></span>

## <span data-ttu-id="5fea1-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5fea1-121">OUTPUTS</span></span>

## <span data-ttu-id="5fea1-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="5fea1-122">NOTES</span></span>

## <span data-ttu-id="5fea1-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5fea1-123">RELATED LINKS</span></span>

[<span data-ttu-id="5fea1-124">Get-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5fea1-124">Get-AzureRmSiteRecoveryVault</span></span>](./Get-AzureRmSiteRecoveryVault.md)

[<span data-ttu-id="5fea1-125">Remove-AzureRmSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="5fea1-125">Remove-AzureRmSiteRecoveryVault</span></span>](./Remove-AzureRmSiteRecoveryVault.md)
