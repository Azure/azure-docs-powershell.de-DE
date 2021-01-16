---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98297503"
---
# <span data-ttu-id="aba35-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aba35-101">Set-AzMediaService</span></span>

## <span data-ttu-id="aba35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba35-102">SYNOPSIS</span></span>
<span data-ttu-id="aba35-103">Ändert die angegebenen Eigenschaften eines vorhandenen Mediendiensts.</span><span class="sxs-lookup"><span data-stu-id="aba35-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="aba35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="aba35-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aba35-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aba35-105">DESCRIPTION</span></span>
<span data-ttu-id="aba35-106">Das **Cmdlet "Set-AzMediaService"** ändert die angegebenen Eigenschaften eines vorhandenen Mediendiensts.</span><span class="sxs-lookup"><span data-stu-id="aba35-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="aba35-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="aba35-107">EXAMPLES</span></span>

### <span data-ttu-id="aba35-108">Beispiel 1: Ändern eines vorhandenen Mediendiensts</span><span class="sxs-lookup"><span data-stu-id="aba35-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="aba35-109">Der erste Befehl erstellt eine Reihe von Tags und speichert diese Tags in der Variablen namens $Tags.</span><span class="sxs-lookup"><span data-stu-id="aba35-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="aba35-110">Mit diesem zweiten Befehl wird der Mediendienst mit dem Namen "MediaService001" aktualisiert, der zur Ressourcengruppe "ResourceGroup123" gehört, mit den in der variablen $Tags gespeicherten Tags.</span><span class="sxs-lookup"><span data-stu-id="aba35-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="aba35-111">Der Befehl verwendet außerdem ein Array von Speicherkonfigurationsobjekten, die in einer $StorageAccounts gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="aba35-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="aba35-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aba35-112">PARAMETERS</span></span>

### <span data-ttu-id="aba35-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="aba35-113">-AccountName</span></span>
<span data-ttu-id="aba35-114">Gibt den Namen des Mediendiensts an, den dieses Cmdlet ändert.</span><span class="sxs-lookup"><span data-stu-id="aba35-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="aba35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba35-115">-DefaultProfile</span></span>
<span data-ttu-id="aba35-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="aba35-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aba35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba35-117">-ResourceGroupName</span></span>
<span data-ttu-id="aba35-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="aba35-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="aba35-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="aba35-119">-StorageAccounts</span></span>
<span data-ttu-id="aba35-120">Gibt ein Array von Speicherkonten an, das dieses Cmdlet dem Mediendienst zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="aba35-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba35-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="aba35-121">-Tag</span></span>
<span data-ttu-id="aba35-122">Die dem Medienkonto zugeordneten Tags.</span><span class="sxs-lookup"><span data-stu-id="aba35-122">The tags associated with the media account.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aba35-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aba35-123">-Confirm</span></span>
<span data-ttu-id="aba35-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aba35-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba35-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="aba35-125">-WhatIf</span></span>
<span data-ttu-id="aba35-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aba35-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba35-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aba35-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba35-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba35-128">CommonParameters</span></span>
<span data-ttu-id="aba35-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba35-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba35-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba35-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba35-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="aba35-131">INPUTS</span></span>

### <span data-ttu-id="aba35-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aba35-132">System.String</span></span>

### <span data-ttu-id="aba35-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aba35-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aba35-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="aba35-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="aba35-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="aba35-135">OUTPUTS</span></span>

### <span data-ttu-id="aba35-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="aba35-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="aba35-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="aba35-137">NOTES</span></span>

## <span data-ttu-id="aba35-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="aba35-138">RELATED LINKS</span></span>

[<span data-ttu-id="aba35-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aba35-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="aba35-140">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aba35-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="aba35-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="aba35-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


