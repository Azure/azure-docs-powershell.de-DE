---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzLogProfile.md
ms.openlocfilehash: 3c8dda7d7b84ae4ee7017c88e211b2ab5db46360
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845108"
---
# <span data-ttu-id="c2ed3-101">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c2ed3-101">Remove-AzLogProfile</span></span>

## <span data-ttu-id="c2ed3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ed3-103">Entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-103">Removes a log profile.</span></span>

## <span data-ttu-id="c2ed3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2ed3-104">SYNTAX</span></span>

```
Remove-AzLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2ed3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ed3-106">Das Cmdlet **Remove-AzLogProfile** entfernt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-106">The **Remove-AzLogProfile** cmdlet removes a log profile.</span></span>
<span data-ttu-id="c2ed3-107">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c2ed3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2ed3-108">EXAMPLES</span></span>

## <span data-ttu-id="c2ed3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ed3-109">PARAMETERS</span></span>

### <span data-ttu-id="c2ed3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ed3-110">-DefaultProfile</span></span>
<span data-ttu-id="c2ed3-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c2ed3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2ed3-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c2ed3-112">-Name</span></span>
<span data-ttu-id="c2ed3-113">Gibt den Namen des zu entfernenden Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-113">Specifies the name of the log profile to remove.</span></span>

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

### <span data-ttu-id="c2ed3-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2ed3-114">-PassThru</span></span>
<span data-ttu-id="c2ed3-115">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c2ed3-115">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2ed3-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2ed3-116">-Confirm</span></span>
<span data-ttu-id="c2ed3-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ed3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ed3-118">-WhatIf</span></span>
<span data-ttu-id="c2ed3-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2ed3-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ed3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ed3-121">CommonParameters</span></span>
<span data-ttu-id="c2ed3-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ed3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ed3-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2ed3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ed3-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2ed3-124">INPUTS</span></span>

### <span data-ttu-id="c2ed3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ed3-125">System.String</span></span>

## <span data-ttu-id="c2ed3-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2ed3-126">OUTPUTS</span></span>

### <span data-ttu-id="c2ed3-127">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c2ed3-127">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="c2ed3-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2ed3-128">NOTES</span></span>

## <span data-ttu-id="c2ed3-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2ed3-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2ed3-130">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c2ed3-130">Add-AzLogProfile</span></span>](./Add-AzLogProfile.md)

[<span data-ttu-id="c2ed3-131">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="c2ed3-131">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)


