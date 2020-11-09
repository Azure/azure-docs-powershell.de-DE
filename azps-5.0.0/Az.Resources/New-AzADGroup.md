---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301017"
---
# <span data-ttu-id="ff6b7-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="ff6b7-101">New-AzADGroup</span></span>

## <span data-ttu-id="ff6b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff6b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6b7-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="ff6b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff6b7-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff6b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff6b7-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6b7-106">Erstellt eine neue Active Directory-Gruppe. Im folgenden finden Sie die erforderlichen Berechtigungen:</span><span class="sxs-lookup"><span data-stu-id="ff6b7-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="ff6b7-107">Azure Active Directory-Diagramm</span><span class="sxs-lookup"><span data-stu-id="ff6b7-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="ff6b7-108">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="ff6b7-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="ff6b7-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="ff6b7-109">Microsoft Graph</span></span>
  - <span data-ttu-id="ff6b7-110">Directory. ReadWrite. all</span><span class="sxs-lookup"><span data-stu-id="ff6b7-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="ff6b7-111">PrivilegedAccess. ReadWrite. AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="ff6b7-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="ff6b7-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff6b7-112">EXAMPLES</span></span>

### <span data-ttu-id="ff6b7-113">Beispiel 1: Erstellen einer neuen Anzeigengruppe</span><span class="sxs-lookup"><span data-stu-id="ff6b7-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="ff6b7-114">Erstellt eine neue Anzeigengruppe mit dem Namen "MyGroupDisplayName" und dem e-Mail-Spitznamen "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="ff6b7-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="ff6b7-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff6b7-115">PARAMETERS</span></span>

### <span data-ttu-id="ff6b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6b7-116">-DefaultProfile</span></span>
<span data-ttu-id="ff6b7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff6b7-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff6b7-118">-Description</span></span>
<span data-ttu-id="ff6b7-119">Die Beschreibung für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-119">The description for the group.</span></span>

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

### <span data-ttu-id="ff6b7-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ff6b7-120">-DisplayName</span></span>
<span data-ttu-id="ff6b7-121">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-121">The display name for the group.</span></span>

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

### <span data-ttu-id="ff6b7-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ff6b7-122">-MailNickname</span></span>
<span data-ttu-id="ff6b7-123">Der e-Mail-Spitznamen für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-123">The mail nickname for the group.</span></span> <span data-ttu-id="ff6b7-124">Das @-Zeichen darf nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="ff6b7-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff6b7-125">-Confirm</span></span>
<span data-ttu-id="ff6b7-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff6b7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff6b7-127">-WhatIf</span></span>
<span data-ttu-id="ff6b7-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff6b7-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff6b7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6b7-130">CommonParameters</span></span>
<span data-ttu-id="ff6b7-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6b7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6b7-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff6b7-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6b7-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff6b7-133">INPUTS</span></span>

### <span data-ttu-id="ff6b7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ff6b7-134">System.String</span></span>

## <span data-ttu-id="ff6b7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff6b7-135">OUTPUTS</span></span>

### <span data-ttu-id="ff6b7-136">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ff6b7-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ff6b7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff6b7-137">NOTES</span></span>

## <span data-ttu-id="ff6b7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff6b7-138">RELATED LINKS</span></span>
