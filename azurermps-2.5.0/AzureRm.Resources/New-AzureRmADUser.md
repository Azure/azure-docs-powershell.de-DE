---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 5a1f0b5bac62c4b10912fbbffc07cda7c1f2fb7b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849892"
---
# <span data-ttu-id="ddd5b-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ddd5b-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="ddd5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ddd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd5b-103">Erstellt einen neuen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddd5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd5b-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddd5b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ddd5b-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd5b-106">Erstellt einen neuen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="ddd5b-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ddd5b-107">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ddd5b-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ddd5b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ddd5b-108">EXAMPLES</span></span>

### <span data-ttu-id="ddd5b-109">Beispiel 1: Erstellen eines neuen anzeigen Benutzers</span><span class="sxs-lookup"><span data-stu-id="ddd5b-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="ddd5b-110">Erstellt einen neuen anzeigen Benutzer mit dem Namen "mydisplayname" und dem Benutzerprinzipalnamen " myemail@domain.com " in einem Mandanten.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="ddd5b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ddd5b-111">PARAMETERS</span></span>

### <span data-ttu-id="ddd5b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd5b-112">-DefaultProfile</span></span>
<span data-ttu-id="ddd5b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ddd5b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddd5b-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ddd5b-114">-DisplayName</span></span>
<span data-ttu-id="ddd5b-115">Der Name, der im Adressbuch für den Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ddd5b-116">Beispiel ' Alex Wu '</span><span class="sxs-lookup"><span data-stu-id="ddd5b-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="ddd5b-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ddd5b-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ddd5b-118">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern muss (wahr).</span><span class="sxs-lookup"><span data-stu-id="ddd5b-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ddd5b-119">Standardverhalten ist (falsch), um das Kennwort bei der nächsten erfolgreichen Anmeldung nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="ddd5b-120">-Unveränderlich</span><span class="sxs-lookup"><span data-stu-id="ddd5b-120">-ImmutableId</span></span>
<span data-ttu-id="ddd5b-121">Sie muss nur angegeben werden, wenn Sie eine Verbunddomäne für die Benutzerprinzipalnamen-Eigenschaft (User Principal Name, UPN) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="ddd5b-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ddd5b-122">-MailNickname</span></span>
<span data-ttu-id="ddd5b-123">Der e-Mail-Alias für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="ddd5b-124">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="ddd5b-124">-Password</span></span>
<span data-ttu-id="ddd5b-125">Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-125">Password for the user.</span></span>
<span data-ttu-id="ddd5b-126">Das Kennwort muss den Komplexitätsanforderungen des Mandanten genügen.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ddd5b-127">Es wird empfohlen, ein sicheres Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="ddd5b-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ddd5b-128">-UserPrincipalName</span></span>
<span data-ttu-id="ddd5b-129">Der Benutzerprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-129">The user principal name.</span></span>
<span data-ttu-id="ddd5b-130">Beispiel: " someuser@contoso.com ".</span><span class="sxs-lookup"><span data-stu-id="ddd5b-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="ddd5b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ddd5b-131">-Confirm</span></span>
<span data-ttu-id="ddd5b-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd5b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd5b-133">-WhatIf</span></span>
<span data-ttu-id="ddd5b-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd5b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd5b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd5b-136">CommonParameters</span></span>
<span data-ttu-id="ddd5b-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd5b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd5b-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd5b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd5b-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ddd5b-139">INPUTS</span></span>

### <span data-ttu-id="ddd5b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd5b-140">System.String</span></span>

### <span data-ttu-id="ddd5b-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ddd5b-141">System.Security.SecureString</span></span>

### <span data-ttu-id="ddd5b-142">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="ddd5b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ddd5b-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ddd5b-143">OUTPUTS</span></span>

### <span data-ttu-id="ddd5b-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ddd5b-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ddd5b-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="ddd5b-145">NOTES</span></span>

## <span data-ttu-id="ddd5b-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ddd5b-146">RELATED LINKS</span></span>

[<span data-ttu-id="ddd5b-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ddd5b-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)



[<span data-ttu-id="ddd5b-148">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ddd5b-148">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
