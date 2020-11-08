---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009503"
---
# <span data-ttu-id="0763f-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0763f-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="0763f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0763f-102">SYNOPSIS</span></span>

## <span data-ttu-id="0763f-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="0763f-103">SYNTAX</span></span>

### <span data-ttu-id="0763f-104">S1</span><span class="sxs-lookup"><span data-stu-id="0763f-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0763f-105">S2</span><span class="sxs-lookup"><span data-stu-id="0763f-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0763f-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0763f-106">DESCRIPTION</span></span>
<span data-ttu-id="0763f-107">Das Cmdlet **Reset-AzWebAppPublishingProfile** setzt das Veröffentlichungsprofil für die angegebene Web-App zurück.</span><span class="sxs-lookup"><span data-stu-id="0763f-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="0763f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0763f-108">EXAMPLES</span></span>

### <span data-ttu-id="0763f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0763f-109">Example 1</span></span>

<span data-ttu-id="0763f-110">Im folgenden Beispiel wird das Veröffentlichungsprofil für das Web-App-IpRule zurückgesetzt, das der Ressourcengruppe myresourcegroup zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0763f-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="0763f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0763f-111">PARAMETERS</span></span>

### <span data-ttu-id="0763f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0763f-112">-DefaultProfile</span></span>
<span data-ttu-id="0763f-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0763f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0763f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0763f-114">-Name</span></span>
<span data-ttu-id="0763f-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="0763f-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0763f-116">-ResourceGroupName</span></span>
<span data-ttu-id="0763f-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="0763f-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-118">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="0763f-118">-WebApp</span></span>
<span data-ttu-id="0763f-119">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="0763f-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0763f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0763f-120">CommonParameters</span></span>
<span data-ttu-id="0763f-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0763f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0763f-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0763f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0763f-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0763f-123">INPUTS</span></span>

### <span data-ttu-id="0763f-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0763f-124">System.String</span></span>

### <span data-ttu-id="0763f-125">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0763f-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0763f-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0763f-126">OUTPUTS</span></span>

### <span data-ttu-id="0763f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0763f-127">System.String</span></span>

## <span data-ttu-id="0763f-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0763f-128">NOTES</span></span>

## <span data-ttu-id="0763f-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0763f-129">RELATED LINKS</span></span>
