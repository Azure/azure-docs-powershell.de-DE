---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363291"
---
# <span data-ttu-id="305ad-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="305ad-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="305ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="305ad-102">SYNOPSIS</span></span>
<span data-ttu-id="305ad-103">Entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="305ad-103">Removes a media service.</span></span>

## <span data-ttu-id="305ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="305ad-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="305ad-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="305ad-105">DESCRIPTION</span></span>
<span data-ttu-id="305ad-106">Das **Cmdlet "Remove-AzMediaService"** entfernt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="305ad-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="305ad-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="305ad-107">EXAMPLES</span></span>

### <span data-ttu-id="305ad-108">Beispiel 1: Entfernen eines Mediendiensts</span><span class="sxs-lookup"><span data-stu-id="305ad-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="305ad-109">Mit diesem Befehl wird der Mediendienst mit dem Namen "MediaService0011" in der Ressourcengruppe "ResourceGroup001" entfernt.</span><span class="sxs-lookup"><span data-stu-id="305ad-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="305ad-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="305ad-110">PARAMETERS</span></span>

### <span data-ttu-id="305ad-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="305ad-111">-AccountName</span></span>
<span data-ttu-id="305ad-112">Gibt den Namen des Mediendiensts an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="305ad-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="305ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="305ad-113">-DefaultProfile</span></span>
<span data-ttu-id="305ad-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="305ad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="305ad-115">-Force</span><span class="sxs-lookup"><span data-stu-id="305ad-115">-Force</span></span>
<span data-ttu-id="305ad-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="305ad-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="305ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="305ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="305ad-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="305ad-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="305ad-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="305ad-119">-Confirm</span></span>
<span data-ttu-id="305ad-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="305ad-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="305ad-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="305ad-121">-WhatIf</span></span>
<span data-ttu-id="305ad-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="305ad-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="305ad-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="305ad-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="305ad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="305ad-124">CommonParameters</span></span>
<span data-ttu-id="305ad-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="305ad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="305ad-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="305ad-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="305ad-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="305ad-127">INPUTS</span></span>

### <span data-ttu-id="305ad-128">System.String</span><span class="sxs-lookup"><span data-stu-id="305ad-128">System.String</span></span>

## <span data-ttu-id="305ad-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="305ad-129">OUTPUTS</span></span>

### <span data-ttu-id="305ad-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="305ad-130">System.Boolean</span></span>

## <span data-ttu-id="305ad-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="305ad-131">NOTES</span></span>

## <span data-ttu-id="305ad-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="305ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="305ad-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="305ad-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="305ad-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="305ad-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="305ad-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="305ad-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


