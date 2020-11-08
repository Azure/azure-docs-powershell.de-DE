---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D35C580F-437A-40F9-B6BA-412A1176292A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9821602df196604100de5926a7d9510bdb011bd2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005887"
---
# <span data-ttu-id="f2a95-101">Export-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-101">Export-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="f2a95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2a95-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a95-103">Exportiert das Vorlagenbild einer Azure RemoteApp-Sammlung in das angegebene Azure-Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f2a95-103">Exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="f2a95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2a95-104">SYNTAX</span></span>

```
Export-AzureRemoteAppTemplateImage [-CollectionName] <String> [-DestinationStorageAccountName] <String>
 [-DestinationStorageAccountKey] <String> [-DestinationStorageAccountContainerName] <String>
 [-OverwriteExistingTemplateImage] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a95-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2a95-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a95-106">Das Cmdlet **Export-AzureRemoteAppTemplateImage** exportiert das Vorlagenbild einer Azure RemoteApp-Sammlung in das angegebene Azure-Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="f2a95-106">The **Export-AzureRemoteAppTemplateImage** cmdlet exports the template image of one Azure RemoteApp collection to the specified Azure storage account.</span></span>

## <span data-ttu-id="f2a95-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2a95-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a95-108">Beispiel 1: Exportieren eines Vorlagenbilds in das Azure-Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f2a95-108">Example 1: Export a template image to the Azure storage account</span></span>
```
PS C:\> Export-AzureRemoteAppTemplateImage -CollectionName "Contoso" -DestinationStorageAccountName "AccountName" -DestinationStorageAccountKey "AccountKey" -DestinationStorageAccountContainerName "ContainerName" -OverwriteExistingTemplateImage
```

<span data-ttu-id="f2a95-109">Mit diesem Befehl wird das Vorlagenbild der Sammlung mit dem Namen "Contoso" in einen Container namens "Containername" im angegebenen Azure-Speicherkonto mit Name Accountname und Key AccountKey exportiert.</span><span class="sxs-lookup"><span data-stu-id="f2a95-109">This command exports the template image of the collection named Contoso to a container named ContainerName in the specified Azure storage account with name AccountName and key AccountKey.</span></span>

## <span data-ttu-id="f2a95-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2a95-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a95-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f2a95-111">-CollectionName</span></span>
<span data-ttu-id="f2a95-112">Gibt den Namen der Quell Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="f2a95-112">Specifies the name of the source Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-113">-DestinationStorageAccountContainerName</span><span class="sxs-lookup"><span data-stu-id="f2a95-113">-DestinationStorageAccountContainerName</span></span>
<span data-ttu-id="f2a95-114">Gibt den Namen eines Containers im Ziel Azure Storage-Konto an.</span><span class="sxs-lookup"><span data-stu-id="f2a95-114">Specifies the name of a container in the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-115">-DestinationStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f2a95-115">-DestinationStorageAccountKey</span></span>
<span data-ttu-id="f2a95-116">Gibt den Schlüssel des Ziels Azure Storage-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f2a95-116">Specifies the key of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-117">-DestinationStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f2a95-117">-DestinationStorageAccountName</span></span>
<span data-ttu-id="f2a95-118">Gibt den Namen des Ziels Azure Storage-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f2a95-118">Specifies the name of the destination Azure storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-119">-OverwriteExistingTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-119">-OverwriteExistingTemplateImage</span></span>
<span data-ttu-id="f2a95-120">Gibt an, dass das Cmdlet das vorhandene Vorlagenbild überschreibt.</span><span class="sxs-lookup"><span data-stu-id="f2a95-120">Indicates that the cmdlet overwrites the existing template image.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="f2a95-121">-Profile</span></span>
<span data-ttu-id="f2a95-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f2a95-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f2a95-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f2a95-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a95-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f2a95-124">-Confirm</span></span>
<span data-ttu-id="f2a95-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2a95-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a95-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a95-126">-WhatIf</span></span>
<span data-ttu-id="f2a95-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2a95-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a95-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f2a95-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a95-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a95-129">CommonParameters</span></span>
<span data-ttu-id="f2a95-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a95-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a95-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a95-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a95-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2a95-132">INPUTS</span></span>

## <span data-ttu-id="f2a95-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2a95-133">OUTPUTS</span></span>

## <span data-ttu-id="f2a95-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2a95-134">NOTES</span></span>

## <span data-ttu-id="f2a95-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2a95-135">RELATED LINKS</span></span>

[<span data-ttu-id="f2a95-136">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-136">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="f2a95-137">Neu – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-137">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="f2a95-138">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-138">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="f2a95-139">Umbenennen – AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="f2a95-139">Rename-AzureRemoteAppTemplateImage</span></span>](./Rename-AzureRemoteAppTemplateImage.md)


