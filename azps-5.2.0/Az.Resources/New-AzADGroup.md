---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 98d87c060c51d19db45e907f88d39f27350248c9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358083"
---
# <span data-ttu-id="3359a-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="3359a-101">New-AzADGroup</span></span>

## <span data-ttu-id="3359a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3359a-102">SYNOPSIS</span></span>
<span data-ttu-id="3359a-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3359a-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="3359a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3359a-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3359a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3359a-105">DESCRIPTION</span></span>
<span data-ttu-id="3359a-106">Erstellt eine neue Active Directory-Gruppe. Im Folgenden sind die erforderlichen Berechtigungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3359a-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="3359a-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="3359a-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="3359a-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3359a-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="3359a-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="3359a-109">Microsoft Graph</span></span>
  - <span data-ttu-id="3359a-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3359a-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="3359a-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="3359a-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="3359a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3359a-112">EXAMPLES</span></span>

### <span data-ttu-id="3359a-113">Beispiel 1: Erstellen einer neuen Ad-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3359a-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="3359a-114">Erstellt eine neue Ad-Gruppe mit dem Namen "MyGroupDisplayName" und dem E-Mail-Spitznamen "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="3359a-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="3359a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3359a-115">PARAMETERS</span></span>

### <span data-ttu-id="3359a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3359a-116">-DefaultProfile</span></span>
<span data-ttu-id="3359a-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3359a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3359a-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3359a-118">-Description</span></span>
<span data-ttu-id="3359a-119">Die Beschreibung für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3359a-119">The description for the group.</span></span>

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

### <span data-ttu-id="3359a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3359a-120">-DisplayName</span></span>
<span data-ttu-id="3359a-121">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3359a-121">The display name for the group.</span></span>

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

### <span data-ttu-id="3359a-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="3359a-122">-MailNickname</span></span>
<span data-ttu-id="3359a-123">Der E-Mail-Alias für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3359a-123">The mail nickname for the group.</span></span> <span data-ttu-id="3359a-124">Darf das @-Zeichen nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="3359a-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="3359a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3359a-125">-Confirm</span></span>
<span data-ttu-id="3359a-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3359a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3359a-127">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3359a-127">-WhatIf</span></span>
<span data-ttu-id="3359a-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3359a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3359a-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3359a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3359a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3359a-130">CommonParameters</span></span>
<span data-ttu-id="3359a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3359a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3359a-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3359a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3359a-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3359a-133">INPUTS</span></span>

### <span data-ttu-id="3359a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3359a-134">System.String</span></span>

## <span data-ttu-id="3359a-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3359a-135">OUTPUTS</span></span>

### <span data-ttu-id="3359a-136">Microsoft.Azure.Commands.ActiveDirectory.WERDENDGroup</span><span class="sxs-lookup"><span data-stu-id="3359a-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="3359a-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3359a-137">NOTES</span></span>

## <span data-ttu-id="3359a-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3359a-138">RELATED LINKS</span></span>
