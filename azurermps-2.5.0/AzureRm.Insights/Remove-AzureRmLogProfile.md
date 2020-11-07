---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 78d2bff42382564bb07f680b5db8db39707ffb97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848279"
---
# <span data-ttu-id="3feb5-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3feb5-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="3feb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3feb5-102">SYNOPSIS</span></span>
<span data-ttu-id="3feb5-103">Entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="3feb5-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3feb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3feb5-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3feb5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3feb5-105">DESCRIPTION</span></span>
<span data-ttu-id="3feb5-106">Das Cmdlet **Remove-AzureRmLogProfile** entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="3feb5-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="3feb5-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="3feb5-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="3feb5-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3feb5-108">EXAMPLES</span></span>

## <span data-ttu-id="3feb5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3feb5-109">PARAMETERS</span></span>

### <span data-ttu-id="3feb5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3feb5-110">-DefaultProfile</span></span>
<span data-ttu-id="3feb5-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3feb5-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3feb5-112">-Name</span><span class="sxs-lookup"><span data-stu-id="3feb5-112">-Name</span></span>
<span data-ttu-id="3feb5-113">Gibt den Namen des zu entfernenden Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="3feb5-113">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3feb5-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3feb5-114">-PassThru</span></span>
<span data-ttu-id="3feb5-115">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3feb5-115">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb5-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3feb5-116">-Confirm</span></span>
<span data-ttu-id="3feb5-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3feb5-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3feb5-118">-WhatIf</span></span>
<span data-ttu-id="3feb5-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3feb5-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3feb5-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3feb5-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3feb5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3feb5-121">CommonParameters</span></span>
<span data-ttu-id="3feb5-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3feb5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3feb5-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3feb5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3feb5-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3feb5-124">INPUTS</span></span>

### <span data-ttu-id="3feb5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3feb5-125">System.String</span></span>

## <span data-ttu-id="3feb5-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3feb5-126">OUTPUTS</span></span>

### <span data-ttu-id="3feb5-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3feb5-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="3feb5-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3feb5-128">NOTES</span></span>

## <span data-ttu-id="3feb5-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3feb5-129">RELATED LINKS</span></span>

[<span data-ttu-id="3feb5-130">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3feb5-130">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="3feb5-131">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="3feb5-131">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


