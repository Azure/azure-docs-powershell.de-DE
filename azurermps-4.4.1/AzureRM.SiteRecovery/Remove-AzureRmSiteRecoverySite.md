---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DE1D5A0D-2545-4F01-98B5-684ED0D25230
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoverySite.md
ms.openlocfilehash: f052b11a11fa77047d424b7045b127a75043cc25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663522"
---
# <span data-ttu-id="e3498-101">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e3498-101">Remove-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="e3498-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e3498-102">SYNOPSIS</span></span>
<span data-ttu-id="e3498-103">Entfernt eine Website Wiederherstellungs Website aus dem aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="e3498-103">Removes a Site Recovery site from the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3498-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3498-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoverySite -Site <ASRSite> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3498-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3498-105">DESCRIPTION</span></span>
<span data-ttu-id="e3498-106">Das Cmdlet **Remove-AzureRmSiteRecoverySite** löscht eine Azure Site Recovery-Website aus dem aktuellen Tresor.</span><span class="sxs-lookup"><span data-stu-id="e3498-106">The **Remove-AzureRmSiteRecoverySite** cmdlet deletes an Azure Site Recovery site from the current vault.</span></span>

## <span data-ttu-id="e3498-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3498-107">EXAMPLES</span></span>

## <span data-ttu-id="e3498-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3498-108">PARAMETERS</span></span>

### <span data-ttu-id="e3498-109">-Force</span><span class="sxs-lookup"><span data-stu-id="e3498-109">-Force</span></span>
<span data-ttu-id="e3498-110">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="e3498-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3498-111">-Website</span><span class="sxs-lookup"><span data-stu-id="e3498-111">-Site</span></span>
<span data-ttu-id="e3498-112">Gibt das Website-Wiederherstellungs Website-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e3498-112">Specifies the Site Recovery site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRSite
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3498-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e3498-113">-Confirm</span></span>
<span data-ttu-id="e3498-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3498-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3498-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3498-115">-WhatIf</span></span>
<span data-ttu-id="e3498-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3498-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e3498-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3498-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3498-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3498-118">-DefaultProfile</span></span>
<span data-ttu-id="e3498-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e3498-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3498-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3498-120">CommonParameters</span></span>
<span data-ttu-id="e3498-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3498-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3498-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3498-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3498-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e3498-123">INPUTS</span></span>

### <span data-ttu-id="e3498-124">ASRSite</span><span class="sxs-lookup"><span data-stu-id="e3498-124">ASRSite</span></span>
<span data-ttu-id="e3498-125">Der Parameter "Website" akzeptiert den Wert vom Typ "ASRSite" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3498-125">Parameter 'Site' accepts value of type 'ASRSite' from the pipeline</span></span>

## <span data-ttu-id="e3498-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e3498-126">OUTPUTS</span></span>

## <span data-ttu-id="e3498-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="e3498-127">NOTES</span></span>

## <span data-ttu-id="e3498-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e3498-128">RELATED LINKS</span></span>

[<span data-ttu-id="e3498-129">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e3498-129">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="e3498-130">Neu – AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="e3498-130">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)
