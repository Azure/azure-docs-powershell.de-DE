---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6E369BDF-AE3C-416B-81B7-097C20147CBE
online version: ''
schema: 2.0.0
ms.openlocfilehash: bb48f7412c957ceefb7df03d79e57ce8e75447d5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006336"
---
# <span data-ttu-id="c7ade-101">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="c7ade-101">Remove-AzureSBNamespace</span></span>

## <span data-ttu-id="c7ade-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7ade-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ade-103">Entfernt einen Namespace.</span><span class="sxs-lookup"><span data-stu-id="c7ade-103">Removes a namespace.</span></span>

## <span data-ttu-id="c7ade-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7ade-104">SYNTAX</span></span>

```
Remove-AzureSBNamespace -Name <String> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7ade-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7ade-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ade-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c7ade-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c7ade-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="c7ade-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c7ade-108">Das Cmdlet " **Remove-AzureSBNamespace** " entfernt einen Dienstnamespace für ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="c7ade-108">The **Remove-AzureSBNamespace** cmdlet removes a service namespace for Service Bus.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="c7ade-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7ade-109">EXAMPLES</span></span>

## <span data-ttu-id="c7ade-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7ade-110">PARAMETERS</span></span>

### <span data-ttu-id="c7ade-111">-Force</span><span class="sxs-lookup"><span data-stu-id="c7ade-111">-Force</span></span>
<span data-ttu-id="c7ade-112">Wenn diese Option aktiviert ist, wird der Namespace entfernt, ohne dass eine Bestätigung angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c7ade-112">If enabled, removes the namespace without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c7ade-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c7ade-113">-Name</span></span>
<span data-ttu-id="c7ade-114">Gibt den Namen des Namespace an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c7ade-114">Specifies the name of the namespace to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7ade-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7ade-115">-PassThru</span></span>
<span data-ttu-id="c7ade-116">Bewirkt, dass der Vorgang true zurückgibt, wenn er erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c7ade-116">Causes the operation to return true if it succeeds.</span></span>

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

### <span data-ttu-id="c7ade-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="c7ade-117">-Profile</span></span>
<span data-ttu-id="c7ade-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c7ade-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c7ade-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c7ade-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c7ade-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c7ade-120">-Confirm</span></span>
<span data-ttu-id="c7ade-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c7ade-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7ade-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ade-122">-WhatIf</span></span>
<span data-ttu-id="c7ade-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c7ade-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ade-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c7ade-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7ade-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ade-125">CommonParameters</span></span>
<span data-ttu-id="c7ade-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ade-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ade-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ade-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ade-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7ade-128">INPUTS</span></span>

## <span data-ttu-id="c7ade-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7ade-129">OUTPUTS</span></span>

## <span data-ttu-id="c7ade-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7ade-130">NOTES</span></span>

## <span data-ttu-id="c7ade-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7ade-131">RELATED LINKS</span></span>

[<span data-ttu-id="c7ade-132">Neu – AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="c7ade-132">New-AzureSBNamespace</span></span>](./New-AzureSBNamespace.md)


