---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaService.md
ms.openlocfilehash: 5b85e3e64b4a79b33975d9b29d0498ac8ae0ce03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180291"
---
# <span data-ttu-id="d4a0b-101">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4a0b-101">Set-AzMediaService</span></span>

## <span data-ttu-id="d4a0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a0b-103">Ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-103">Modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="d4a0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a0b-104">SYNTAX</span></span>

```
Set-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a0b-106">Das Cmdlet " **Satz-AzMediaService** " ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-106">The **Set-AzMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="d4a0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a0b-108">Beispiel 1: Ändern eines vorhandenen Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="d4a0b-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tag $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="d4a0b-109">Der erste Befehl erstellt eine Reihe von Tags und speichert diese Tags in der Variablen mit dem Namen $Tags.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>
<span data-ttu-id="d4a0b-110">Dieser zweite Befehl aktualisiert den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup123 gehört, wobei die in $Tags Variablen gespeicherten Tags enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="d4a0b-111">Der Befehl verwendet auch ein Array von Speicher Konfigurationsobjekten, die in $StorageAccounts Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="d4a0b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a0b-112">PARAMETERS</span></span>

### <span data-ttu-id="d4a0b-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d4a0b-113">-AccountName</span></span>
<span data-ttu-id="d4a0b-114">Gibt den Namen des Medien Diensts an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d4a0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a0b-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a0b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4a0b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4a0b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4a0b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d4a0b-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="d4a0b-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d4a0b-119">-StorageAccounts</span></span>
<span data-ttu-id="d4a0b-120">Gibt ein Array von Speicherkonten an, die dieses Cmdlet dem Mediendienst anordnet.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="d4a0b-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4a0b-121">-Tag</span></span>
<span data-ttu-id="d4a0b-122">Die Tags, die dem Medien Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-122">The tags associated with the media account.</span></span>

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

### <span data-ttu-id="d4a0b-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4a0b-123">-Confirm</span></span>
<span data-ttu-id="d4a0b-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a0b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a0b-125">-WhatIf</span></span>
<span data-ttu-id="d4a0b-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a0b-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a0b-128">CommonParameters</span></span>
<span data-ttu-id="d4a0b-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a0b-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a0b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a0b-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4a0b-131">INPUTS</span></span>

### <span data-ttu-id="d4a0b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a0b-132">System.String</span></span>

### <span data-ttu-id="d4a0b-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d4a0b-133">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d4a0b-134">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="d4a0b-134">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="d4a0b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4a0b-135">OUTPUTS</span></span>

### <span data-ttu-id="d4a0b-136">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="d4a0b-136">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="d4a0b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4a0b-137">NOTES</span></span>

## <span data-ttu-id="d4a0b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4a0b-138">RELATED LINKS</span></span>

[<span data-ttu-id="d4a0b-139">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4a0b-139">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="d4a0b-140">Neu – AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4a0b-140">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="d4a0b-141">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="d4a0b-141">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)


