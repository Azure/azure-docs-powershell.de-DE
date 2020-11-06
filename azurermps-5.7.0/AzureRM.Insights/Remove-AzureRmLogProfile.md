---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: a1cb32d619a39b5b1a6fb1cd9c2c5eaa8dde55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481201"
---
# <span data-ttu-id="298f8-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="298f8-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="298f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="298f8-102">SYNOPSIS</span></span>
<span data-ttu-id="298f8-103">Entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="298f8-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="298f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="298f8-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="298f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="298f8-105">DESCRIPTION</span></span>
<span data-ttu-id="298f8-106">Das Cmdlet **Remove-AzureRmLogProfile** entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="298f8-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

<span data-ttu-id="298f8-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="298f8-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="298f8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="298f8-108">EXAMPLES</span></span>

## <span data-ttu-id="298f8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="298f8-109">PARAMETERS</span></span>

### <span data-ttu-id="298f8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="298f8-110">-DefaultProfile</span></span>
<span data-ttu-id="298f8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="298f8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="298f8-112">-Name</span><span class="sxs-lookup"><span data-stu-id="298f8-112">-Name</span></span>
<span data-ttu-id="298f8-113">Gibt den Namen des zu entfernenden Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="298f8-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="298f8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="298f8-114">-PassThru</span></span>
<span data-ttu-id="298f8-115">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="298f8-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="298f8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298f8-116">CommonParameters</span></span>
<span data-ttu-id="298f8-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="298f8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298f8-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="298f8-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298f8-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="298f8-119">INPUTS</span></span>

### <span data-ttu-id="298f8-120">Keine</span><span class="sxs-lookup"><span data-stu-id="298f8-120">None</span></span>
<span data-ttu-id="298f8-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="298f8-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="298f8-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="298f8-122">OUTPUTS</span></span>

### <span data-ttu-id="298f8-123">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="298f8-123">AzureOperationResponse</span></span>

## <span data-ttu-id="298f8-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="298f8-124">NOTES</span></span>

## <span data-ttu-id="298f8-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="298f8-125">RELATED LINKS</span></span>

[<span data-ttu-id="298f8-126">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="298f8-126">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="298f8-127">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="298f8-127">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


