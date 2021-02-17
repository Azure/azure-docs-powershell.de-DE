---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 213e488dde914a8e87b76d6c3765f5dbe99a527a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399973"
---
# <span data-ttu-id="c771d-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c771d-101">New-AzADUser</span></span>

## <span data-ttu-id="c771d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c771d-102">SYNOPSIS</span></span>
<span data-ttu-id="c771d-103">Erstellt einen neuen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c771d-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="c771d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c771d-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c771d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c771d-105">DESCRIPTION</span></span>
<span data-ttu-id="c771d-106">Erstellt einen neuen Active Directory-Benutzer (Arbeits-/Schulkonto, auch als Organisations-ID bekannt).</span><span class="sxs-lookup"><span data-stu-id="c771d-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="c771d-107">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="c771d-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="c771d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c771d-108">EXAMPLES</span></span>

### <span data-ttu-id="c771d-109">Beispiel 1: Erstellen eines neuen Ad-Ad-Benutzers</span><span class="sxs-lookup"><span data-stu-id="c771d-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="c771d-110">Erstellt einen neuen Ad-Benutzer mit dem Namen "MyDisplayName" und dem Benutzerprinzipalnamen " myemail@domain.com " in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="c771d-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="c771d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c771d-111">PARAMETERS</span></span>

### <span data-ttu-id="c771d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c771d-112">-DefaultProfile</span></span>
<span data-ttu-id="c771d-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c771d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c771d-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c771d-114">-DisplayName</span></span>
<span data-ttu-id="c771d-115">Der Name, der im Adressbuch für den Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c771d-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="c771d-116">Beispiel 'Alex Wu'.</span><span class="sxs-lookup"><span data-stu-id="c771d-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="c771d-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="c771d-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="c771d-118">Es muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern muss (true).</span><span class="sxs-lookup"><span data-stu-id="c771d-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="c771d-119">Das Standardverhalten ist "(false)", um das Kennwort bei der nächsten erfolgreichen Anmeldung nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c771d-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c771d-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="c771d-120">-ImmutableId</span></span>
<span data-ttu-id="c771d-121">Er muss nur angegeben werden, wenn Sie eine Verbunddomäne für die Eigenschaft "Benutzerprinzipalname(upn)" des Benutzers verwenden.</span><span class="sxs-lookup"><span data-stu-id="c771d-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="c771d-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="c771d-122">-MailNickname</span></span>
<span data-ttu-id="c771d-123">Der E-Mail-Alias für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c771d-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="c771d-124">-Password</span><span class="sxs-lookup"><span data-stu-id="c771d-124">-Password</span></span>
<span data-ttu-id="c771d-125">Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c771d-125">Password for the user.</span></span>
<span data-ttu-id="c771d-126">Es muss die Anforderungen an die Kennwortkomplexität des Mandanten erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c771d-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="c771d-127">Es wird empfohlen, ein starkes Kennwort zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c771d-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c771d-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c771d-128">-UserPrincipalName</span></span>
<span data-ttu-id="c771d-129">Der Benutzerprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="c771d-129">The user principal name.</span></span>
<span data-ttu-id="c771d-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="c771d-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="c771d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c771d-131">-Confirm</span></span>
<span data-ttu-id="c771d-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c771d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c771d-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c771d-133">-WhatIf</span></span>
<span data-ttu-id="c771d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c771d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c771d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c771d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c771d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c771d-136">CommonParameters</span></span>
<span data-ttu-id="c771d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c771d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c771d-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c771d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c771d-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c771d-139">INPUTS</span></span>

### <span data-ttu-id="c771d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c771d-140">System.String</span></span>

### <span data-ttu-id="c771d-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="c771d-141">System.Security.SecureString</span></span>

### <span data-ttu-id="c771d-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c771d-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c771d-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c771d-143">OUTPUTS</span></span>

### <span data-ttu-id="c771d-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.WERDENDUser</span><span class="sxs-lookup"><span data-stu-id="c771d-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="c771d-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c771d-145">NOTES</span></span>

## <span data-ttu-id="c771d-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c771d-146">RELATED LINKS</span></span>

[<span data-ttu-id="c771d-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c771d-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="c771d-148">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="c771d-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
