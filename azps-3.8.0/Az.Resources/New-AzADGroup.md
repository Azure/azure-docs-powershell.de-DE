---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 6496f2c65c5cfecb01ed68d0e47281fba72b7b63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004665"
---
# <span data-ttu-id="ea34f-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="ea34f-101">New-AzADGroup</span></span>

## <span data-ttu-id="ea34f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea34f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea34f-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ea34f-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="ea34f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea34f-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea34f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea34f-105">DESCRIPTION</span></span>
<span data-ttu-id="ea34f-106">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ea34f-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="ea34f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea34f-107">EXAMPLES</span></span>

### <span data-ttu-id="ea34f-108">Beispiel 1 – Erstellen einer neuen Anzeigengruppe</span><span class="sxs-lookup"><span data-stu-id="ea34f-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="ea34f-109">Erstellt eine neue Anzeigengruppe mit dem Namen "MyGroupDisplayName" und dem e-Mail-Spitznamen "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="ea34f-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="ea34f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea34f-110">PARAMETERS</span></span>

### <span data-ttu-id="ea34f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea34f-111">-DefaultProfile</span></span>
<span data-ttu-id="ea34f-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ea34f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea34f-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea34f-113">-Description</span></span>
<span data-ttu-id="ea34f-114">Die Beschreibung für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ea34f-114">The description for the group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea34f-115">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ea34f-115">-DisplayName</span></span>
<span data-ttu-id="ea34f-116">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ea34f-116">The display name for the group.</span></span>

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

### <span data-ttu-id="ea34f-117">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ea34f-117">-MailNickname</span></span>
<span data-ttu-id="ea34f-118">Der e-Mail-Spitznamen für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ea34f-118">The mail nickname for the group.</span></span> <span data-ttu-id="ea34f-119">Das @-Zeichen darf nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ea34f-119">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="ea34f-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea34f-120">-Confirm</span></span>
<span data-ttu-id="ea34f-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea34f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea34f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea34f-122">-WhatIf</span></span>
<span data-ttu-id="ea34f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea34f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea34f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea34f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea34f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea34f-125">CommonParameters</span></span>
<span data-ttu-id="ea34f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea34f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea34f-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea34f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea34f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea34f-128">INPUTS</span></span>

### <span data-ttu-id="ea34f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ea34f-129">System.String</span></span>

## <span data-ttu-id="ea34f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea34f-130">OUTPUTS</span></span>

### <span data-ttu-id="ea34f-131">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ea34f-131">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ea34f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea34f-132">NOTES</span></span>

## <span data-ttu-id="ea34f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea34f-133">RELATED LINKS</span></span>
