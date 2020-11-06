---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 0FA49058-F3A7-4ED9-93F2-0C84BC130FB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaService.md
ms.openlocfilehash: 19db06ff5563e954124ab36274d62cce0e51b3a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500814"
---
# <span data-ttu-id="3fe6a-101">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe6a-101">Set-AzureRmMediaService</span></span>

## <span data-ttu-id="3fe6a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fe6a-102">SYNOPSIS</span></span>
<span data-ttu-id="3fe6a-103">Ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-103">Modifies specified properties of an existing media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fe6a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fe6a-104">SYNTAX</span></span>

```
Set-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Tags <Hashtable>]
 [-StorageAccounts <PSStorageAccount[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3fe6a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fe6a-105">DESCRIPTION</span></span>
<span data-ttu-id="3fe6a-106">Das Cmdlet " **Satz-AzureRmMediaService** " ändert die angegebenen Eigenschaften eines vorhandenen Medien Diensts.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-106">The **Set-AzureRmMediaService** cmdlet modifies specified properties of an existing media service.</span></span>

## <span data-ttu-id="3fe6a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fe6a-107">EXAMPLES</span></span>

### <span data-ttu-id="3fe6a-108">Beispiel 1: Ändern eines vorhandenen Medien Diensts</span><span class="sxs-lookup"><span data-stu-id="3fe6a-108">Example 1: Modify an existing media service</span></span>
```
PS C:\>$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
Set-AzureRmMediaService -ResourceGroupName "ResourceGroup123" -AccountName "MediaService001" -Tags $Tags -StorageAccounts $StorageAccounts
```

<span data-ttu-id="3fe6a-109">Der erste Befehl erstellt eine Reihe von Tags und speichert diese Tags in der Variablen mit dem Namen $Tags.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-109">The first command creates a series of tags and stores those tags in the variable named $Tags.</span></span>

<span data-ttu-id="3fe6a-110">Dieser zweite Befehl aktualisiert den Mediendienst mit dem Namen MediaService001, der zur Ressourcengruppe mit dem Namen ResourceGroup123 gehört, wobei die in $Tags Variablen gespeicherten Tags enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-110">This second command updates the media service named MediaService001 that belongs to the resource group named ResourceGroup123 with the tags stored in $Tags variable.</span></span>
<span data-ttu-id="3fe6a-111">Der Befehl verwendet auch ein Array von Speicher Konfigurationsobjekten, die in $StorageAccounts Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-111">The command also uses an array of storage configuration objects stored in $StorageAccounts variable.</span></span>

## <span data-ttu-id="3fe6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fe6a-112">PARAMETERS</span></span>

### <span data-ttu-id="3fe6a-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3fe6a-113">-AccountName</span></span>
<span data-ttu-id="3fe6a-114">Gibt den Namen des Medien Diensts an, der vom Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-114">Specifies the name of the media service that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3fe6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fe6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fe6a-116">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="3fe6a-117">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3fe6a-117">-StorageAccounts</span></span>
<span data-ttu-id="3fe6a-118">Gibt ein Array von Speicherkonten an, die dieses Cmdlet dem Mediendienst anordnet.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-118">Specifies an array of storage accounts that this cmdlet associates with the media service.</span></span>

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

### <span data-ttu-id="3fe6a-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="3fe6a-119">-Tags</span></span>
<span data-ttu-id="3fe6a-120">Gibt Tags für den Mediendienst an.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-120">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="3fe6a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fe6a-121">-Confirm</span></span>
<span data-ttu-id="3fe6a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fe6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fe6a-123">-WhatIf</span></span>
<span data-ttu-id="3fe6a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fe6a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fe6a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fe6a-126">-DefaultProfile</span></span>
<span data-ttu-id="3fe6a-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3fe6a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fe6a-128">CommonParameters</span></span>
<span data-ttu-id="3fe6a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fe6a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fe6a-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fe6a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fe6a-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fe6a-131">INPUTS</span></span>

## <span data-ttu-id="3fe6a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fe6a-132">OUTPUTS</span></span>

### <span data-ttu-id="3fe6a-133">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe6a-133">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3fe6a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fe6a-134">NOTES</span></span>

## <span data-ttu-id="3fe6a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fe6a-135">RELATED LINKS</span></span>

[<span data-ttu-id="3fe6a-136">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe6a-136">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="3fe6a-137">Neu – AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe6a-137">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="3fe6a-138">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="3fe6a-138">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)


