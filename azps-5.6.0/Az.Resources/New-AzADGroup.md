---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADGroup.md
ms.openlocfilehash: 910453711e047f9be1694bed0c92c502694d8a6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930851"
---
# <span data-ttu-id="61f11-101">New-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="61f11-101">New-AzADGroup</span></span>

## <span data-ttu-id="61f11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f11-102">SYNOPSIS</span></span>
<span data-ttu-id="61f11-103">Erstellt eine neue Active Directory-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61f11-103">Creates a new active directory group.</span></span>

## <span data-ttu-id="61f11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61f11-104">SYNTAX</span></span>

```
New-AzADGroup -DisplayName <String> -MailNickname <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f11-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61f11-105">DESCRIPTION</span></span>
<span data-ttu-id="61f11-106">Erstellt eine neue Active Directory-Gruppe. Im Folgenden sind die erforderlichen Berechtigungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="61f11-106">Creates a new active directory group.Below are the permissions needed:</span></span>

- <span data-ttu-id="61f11-107">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="61f11-107">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="61f11-108">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61f11-108">Directory.ReadWrite.All</span></span>
- <span data-ttu-id="61f11-109">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="61f11-109">Microsoft Graph</span></span>
  - <span data-ttu-id="61f11-110">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61f11-110">Directory.ReadWrite.All</span></span>
  - <span data-ttu-id="61f11-111">PrivilegedAccess.ReadWrite.AzureADGroup</span><span class="sxs-lookup"><span data-stu-id="61f11-111">PrivilegedAccess.ReadWrite.AzureADGroup</span></span>

## <span data-ttu-id="61f11-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61f11-112">EXAMPLES</span></span>

### <span data-ttu-id="61f11-113">Beispiel 1: Erstellen einer neuen AD-Gruppe</span><span class="sxs-lookup"><span data-stu-id="61f11-113">Example 1: Create a new AD group</span></span>

```powershell
PS C:\> New-AzADGroup -DisplayName "MyGroupDisplayName" -MailNickname "MyGroupNick"
```

<span data-ttu-id="61f11-114">Erstellt eine neue AD-Gruppe mit dem Namen "MyGroupDisplayName" und dem E-Mail-Spitznamen "MyGroupNick".</span><span class="sxs-lookup"><span data-stu-id="61f11-114">Creates a new AD group with the name "MyGroupDisplayName" and the mail nickname "MyGroupNick".</span></span>

## <span data-ttu-id="61f11-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61f11-115">PARAMETERS</span></span>

### <span data-ttu-id="61f11-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f11-116">-DefaultProfile</span></span>
<span data-ttu-id="61f11-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61f11-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f11-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61f11-118">-Description</span></span>
<span data-ttu-id="61f11-119">Die Beschreibung für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61f11-119">The description for the group.</span></span>

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

### <span data-ttu-id="61f11-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61f11-120">-DisplayName</span></span>
<span data-ttu-id="61f11-121">Der Anzeigename für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61f11-121">The display name for the group.</span></span>

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

### <span data-ttu-id="61f11-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="61f11-122">-MailNickname</span></span>
<span data-ttu-id="61f11-123">Der E-Mail-Spitzname für die Gruppe.</span><span class="sxs-lookup"><span data-stu-id="61f11-123">The mail nickname for the group.</span></span> <span data-ttu-id="61f11-124">Das @-Zeichen kann nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="61f11-124">Cannot contain the @ sign.</span></span>

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

### <span data-ttu-id="61f11-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61f11-125">-Confirm</span></span>
<span data-ttu-id="61f11-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61f11-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f11-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f11-127">-WhatIf</span></span>
<span data-ttu-id="61f11-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61f11-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61f11-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61f11-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f11-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f11-130">CommonParameters</span></span>
<span data-ttu-id="61f11-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f11-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f11-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61f11-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f11-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61f11-133">INPUTS</span></span>

### <span data-ttu-id="61f11-134">System.String</span><span class="sxs-lookup"><span data-stu-id="61f11-134">System.String</span></span>

## <span data-ttu-id="61f11-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61f11-135">OUTPUTS</span></span>

### <span data-ttu-id="61f11-136">Microsoft.Azure.Commands.ActiveDirectory.PSDGroup</span><span class="sxs-lookup"><span data-stu-id="61f11-136">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="61f11-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="61f11-137">NOTES</span></span>

## <span data-ttu-id="61f11-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="61f11-138">RELATED LINKS</span></span>
