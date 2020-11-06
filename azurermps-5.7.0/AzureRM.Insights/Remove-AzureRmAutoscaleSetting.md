---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 6140E973-D7AB-4A28-A4FA-818E08129372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 4d6c2f748915847038ef4029dc024763375ef99e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481217"
---
# <span data-ttu-id="0ebde-101">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0ebde-101">Remove-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="0ebde-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ebde-102">SYNOPSIS</span></span>
<span data-ttu-id="0ebde-103">Entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0ebde-103">Removes an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ebde-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ebde-104">SYNTAX</span></span>

```
Remove-AzureRmAutoscaleSetting -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ebde-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ebde-105">DESCRIPTION</span></span>
<span data-ttu-id="0ebde-106">Das Cmdlet **Remove-AzureRmAutoscaleSetting** entfernt eine AutoScale-Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0ebde-106">The **Remove-AzureRmAutoscaleSetting** cmdlet removes an Autoscale setting.</span></span>
<span data-ttu-id="0ebde-107">Sie müssen den Namen der Einstellung und den Namen der Ressourcengruppe angeben, der Sie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0ebde-107">You must specify the name of the setting and the name of the resource group to which it is assigned.</span></span>

<span data-ttu-id="0ebde-108">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0ebde-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="0ebde-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ebde-109">EXAMPLES</span></span>

## <span data-ttu-id="0ebde-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ebde-110">PARAMETERS</span></span>

### <span data-ttu-id="0ebde-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ebde-111">-DefaultProfile</span></span>
<span data-ttu-id="0ebde-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0ebde-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ebde-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0ebde-113">-Name</span></span>
<span data-ttu-id="0ebde-114">Gibt den Namen der zu entfernenden AutoScale-Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="0ebde-114">Specifies the name of the Autoscale setting to remove.</span></span>

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

### <span data-ttu-id="0ebde-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ebde-115">-ResourceGroupName</span></span>
<span data-ttu-id="0ebde-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0ebde-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ebde-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ebde-117">CommonParameters</span></span>
<span data-ttu-id="0ebde-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ebde-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ebde-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ebde-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ebde-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ebde-120">INPUTS</span></span>

### <span data-ttu-id="0ebde-121">Keine</span><span class="sxs-lookup"><span data-stu-id="0ebde-121">None</span></span>
<span data-ttu-id="0ebde-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0ebde-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ebde-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ebde-123">OUTPUTS</span></span>

### <span data-ttu-id="0ebde-124">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0ebde-124">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="0ebde-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ebde-125">NOTES</span></span>

## <span data-ttu-id="0ebde-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ebde-126">RELATED LINKS</span></span>

[<span data-ttu-id="0ebde-127">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0ebde-127">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="0ebde-128">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="0ebde-128">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)


