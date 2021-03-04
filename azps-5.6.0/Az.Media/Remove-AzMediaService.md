---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 5b27574dc6ea60472a16c0b647027ceba17a87b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946055"
---
# <span data-ttu-id="b00be-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b00be-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="b00be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b00be-102">SYNOPSIS</span></span>
<span data-ttu-id="b00be-103">Entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="b00be-103">Removes a media service.</span></span>

## <span data-ttu-id="b00be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b00be-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b00be-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b00be-105">DESCRIPTION</span></span>
<span data-ttu-id="b00be-106">Das **Cmdlet Remove-AzMediaService** entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="b00be-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="b00be-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b00be-107">EXAMPLES</span></span>

### <span data-ttu-id="b00be-108">Beispiel 1: Entfernen eines Mediendiensts</span><span class="sxs-lookup"><span data-stu-id="b00be-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="b00be-109">Mit diesem Befehl wird der Mediendienst mit dem Namen MediaService0011 in der Ressourcengruppe "ResourceGroup001" entfernt.</span><span class="sxs-lookup"><span data-stu-id="b00be-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="b00be-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b00be-110">PARAMETERS</span></span>

### <span data-ttu-id="b00be-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b00be-111">-AccountName</span></span>
<span data-ttu-id="b00be-112">Gibt den Namen des Mediendiensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="b00be-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b00be-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b00be-113">-DefaultProfile</span></span>
<span data-ttu-id="b00be-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b00be-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b00be-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b00be-115">-Force</span></span>
<span data-ttu-id="b00be-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b00be-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b00be-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b00be-117">-ResourceGroupName</span></span>
<span data-ttu-id="b00be-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="b00be-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="b00be-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b00be-119">-Confirm</span></span>
<span data-ttu-id="b00be-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b00be-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b00be-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b00be-121">-WhatIf</span></span>
<span data-ttu-id="b00be-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b00be-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b00be-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b00be-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b00be-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b00be-124">CommonParameters</span></span>
<span data-ttu-id="b00be-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b00be-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b00be-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b00be-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b00be-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b00be-127">INPUTS</span></span>

### <span data-ttu-id="b00be-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b00be-128">System.String</span></span>

## <span data-ttu-id="b00be-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b00be-129">OUTPUTS</span></span>

### <span data-ttu-id="b00be-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b00be-130">System.Boolean</span></span>

## <span data-ttu-id="b00be-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b00be-131">NOTES</span></span>

## <span data-ttu-id="b00be-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b00be-132">RELATED LINKS</span></span>

[<span data-ttu-id="b00be-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b00be-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b00be-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b00be-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="b00be-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b00be-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


