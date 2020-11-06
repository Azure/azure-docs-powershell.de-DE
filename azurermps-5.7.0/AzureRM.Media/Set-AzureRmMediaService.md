---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 413a357d793bd72ff7d1e30cb65e56cb5bd5f3a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496486"
---
# <span data-ttu-id="2b536-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b536-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="2b536-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b536-102">SYNOPSIS</span></span>
<span data-ttu-id="2b536-103">Ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="2b536-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b536-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b536-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tag <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b536-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b536-105">DESCRIPTION</span></span>
<span data-ttu-id="2b536-106">Das Cmdlet " **Satz-AzureRmMediaService** " ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="2b536-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="2b536-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b536-107">EXAMPLES</span></span>

### <span data-ttu-id="2b536-108">Beispiel 1: Ändern eines vorhandenen Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="2b536-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="2b536-109">Der erste Befehl erstellt eine Reihe von Tags und speichert diese Tags in der Variablen mit dem Namen $Tags.</span><span class="sxs-lookup"><span data-stu-id="2b536-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="2b536-110">Dieser zweite Befehl aktualisiert den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup123 gehört, wobei die in $Tags Variablen gespeicherten Tags enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="2b536-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="2b536-111">Der Befehl verwendet auch ein Array von Speicher Konfigurationsobjekten, die in $StorageAccounts Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="2b536-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="2b536-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b536-112">PARAMETERS</span></span>

### <span data-ttu-id="2b536-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="2b536-113">-AccountName</span></span>
<span data-ttu-id="2b536-114">Gibt den Namen des Medien Diensts an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2b536-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b536-115">-DefaultProfile</span></span>
<span data-ttu-id="2b536-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2b536-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b536-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b536-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b536-118">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="2b536-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-119">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2b536-119">-StorageAccounts</span></span>
<span data-ttu-id="2b536-120">Gibt ein Array von Speicherkonten an, die dieses Cmdlet dem Mediendienst anordnet.</span><span class="sxs-lookup"><span data-stu-id="2b536-120">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

```yaml
Type: PSStorageAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b536-121">-Tag</span></span>
<span data-ttu-id="2b536-122">Die Tags, die dem Medien Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2b536-122">The tags associated with the media account.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b536-123">-Confirm</span></span>
<span data-ttu-id="2b536-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b536-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b536-125">-WhatIf</span></span>
<span data-ttu-id="2b536-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b536-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b536-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b536-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b536-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b536-128">CommonParameters</span></span>
<span data-ttu-id="2b536-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b536-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b536-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b536-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b536-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b536-131">INPUTS</span></span>

### <span data-ttu-id="2b536-132">Keine</span><span class="sxs-lookup"><span data-stu-id="2b536-132">None</span></span>
<span data-ttu-id="2b536-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2b536-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b536-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b536-134">OUTPUTS</span></span>

### <span data-ttu-id="2b536-135">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="2b536-135">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="2b536-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b536-136">NOTES</span></span>

## <span data-ttu-id="2b536-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b536-137">RELATED LINKS</span></span>

[<span data-ttu-id="2b536-138">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b536-138">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="2b536-139">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b536-139">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="2b536-140">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b536-140">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


