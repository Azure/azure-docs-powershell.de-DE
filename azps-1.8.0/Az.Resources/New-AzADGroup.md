---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 50cb6a806522e8e8b0f3a792ad74e2543633f668
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659612"
---
# <span data-ttu-id="f253a-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="f253a-101">New-AzADGroup</span></span>

## <span data-ttu-id="f253a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f253a-102">SYNOPSIS</span></span>
<span data-ttu-id="f253a-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f253a-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="f253a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f253a-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f253a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f253a-105">DESCRIPTION</span></span>
<span data-ttu-id="f253a-106">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f253a-106">Creates a new active directory group.</span></span>

## <span data-ttu-id="f253a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f253a-107">EXAMPLES</span></span>

### <span data-ttu-id="f253a-108">Beispiel 1 – Erstellen einer neuen Anzeigengruppe</span><span class="sxs-lookup"><span data-stu-id="f253a-108">Example 1 - Create a new AD group</span></span>

```
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="f253a-109">Erstellt eine neue Anzeigengruppe mit dem Namen "MyGroupDisplayName" und dem e-Mail-Spitznamen "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="f253a-109">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="f253a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f253a-110">PARAMETERS</span></span>

### <span data-ttu-id="f253a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f253a-111">-DefaultProfile</span></span>
<span data-ttu-id="f253a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f253a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f253a-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f253a-113">-DisplayName</span></span>
<span data-ttu-id="f253a-114">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f253a-114">The display name for the group.</span></span>

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

### <span data-ttu-id="f253a-115">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="f253a-115">-MailNickname</span></span>
<span data-ttu-id="f253a-116">Der e-Mail-Spitznamen für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f253a-116">The mail nickname for the group.</span></span> <span data-ttu-id="f253a-117">Das @-Zeichen darf nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="f253a-117">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="f253a-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f253a-118">-Confirm</span></span>
<span data-ttu-id="f253a-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f253a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f253a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f253a-120">-WhatIf</span></span>
<span data-ttu-id="f253a-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f253a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f253a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f253a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f253a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f253a-123">CommonParameters</span></span>
<span data-ttu-id="f253a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f253a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f253a-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f253a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f253a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f253a-126">INPUTS</span></span>

### <span data-ttu-id="f253a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f253a-127">System.String</span></span>

## <span data-ttu-id="f253a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f253a-128">OUTPUTS</span></span>

### <span data-ttu-id="f253a-129">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="f253a-129">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="f253a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f253a-130">NOTES</span></span>

## <span data-ttu-id="f253a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f253a-131">RELATED LINKS</span></span>
