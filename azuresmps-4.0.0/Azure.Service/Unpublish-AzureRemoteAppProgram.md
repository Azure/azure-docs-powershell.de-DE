---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DB3F85D6-5962-4288-AD75-0C30448B769C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88438fa66e39b5ad63db7b6d2609107d224f7faf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006226"
---
# <span data-ttu-id="cd06c-101">Unpublish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="cd06c-101">Unpublish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="cd06c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd06c-102">SYNOPSIS</span></span>
<span data-ttu-id="cd06c-103">Aufheben der Veröffentlichung eines Azure RemoteApp-Programms</span><span class="sxs-lookup"><span data-stu-id="cd06c-103">Unpublishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="cd06c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd06c-104">SYNTAX</span></span>

```
Unpublish-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String[]>] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd06c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd06c-105">DESCRIPTION</span></span>
<span data-ttu-id="cd06c-106">Das Cmdlet " **UNPUBLISH-AzureRemoteAppProgram** " deveröffentlicht ein Azure RemoteApp-Programm.</span><span class="sxs-lookup"><span data-stu-id="cd06c-106">The **Unpublish-AzureRemoteAppProgram** cmdlet unpublishes an Azure RemoteApp program.</span></span>
<span data-ttu-id="cd06c-107">Nachdem Sie die Veröffentlichung eines Programms aufgehoben haben, steht es den Benutzern einer Azure RemoteApp-Sammlung nicht mehr zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cd06c-107">After you unpublish a program, it is no longer available to the users of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="cd06c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd06c-108">EXAMPLES</span></span>

## <span data-ttu-id="cd06c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd06c-109">PARAMETERS</span></span>

### <span data-ttu-id="cd06c-110">-Alias</span><span class="sxs-lookup"><span data-stu-id="cd06c-110">-Alias</span></span>
<span data-ttu-id="cd06c-111">Gibt ein Array von Aliasen der Programme an, deren Veröffentlichung Sie aufheben möchten.</span><span class="sxs-lookup"><span data-stu-id="cd06c-111">Specifies an array of aliases of the programs to unpublish.</span></span>
<span data-ttu-id="cd06c-112">Verwenden **Sie Get-AzureRemoteAppProgram** , um den Alias eines Programms zum Aufheben der Veröffentlichung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cd06c-112">Use **Get-AzureRemoteAppProgram** to retrieve the alias of a program to unpublish.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd06c-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="cd06c-113">-CollectionName</span></span>
<span data-ttu-id="cd06c-114">Gibt den Namen der Azure RemoteApp-Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="cd06c-114">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd06c-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="cd06c-115">-Profile</span></span>
<span data-ttu-id="cd06c-116">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="cd06c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cd06c-117">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="cd06c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cd06c-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cd06c-118">-Confirm</span></span>
<span data-ttu-id="cd06c-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd06c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd06c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd06c-120">-WhatIf</span></span>
<span data-ttu-id="cd06c-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd06c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd06c-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd06c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd06c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd06c-123">CommonParameters</span></span>
<span data-ttu-id="cd06c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd06c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd06c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd06c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd06c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd06c-126">INPUTS</span></span>

## <span data-ttu-id="cd06c-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd06c-127">OUTPUTS</span></span>

## <span data-ttu-id="cd06c-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd06c-128">NOTES</span></span>

## <span data-ttu-id="cd06c-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd06c-129">RELATED LINKS</span></span>

[<span data-ttu-id="cd06c-130">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="cd06c-130">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="cd06c-131">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="cd06c-131">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)


