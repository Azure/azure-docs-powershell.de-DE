---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: ec9c234a03180f20b1b0cf6a4f5004923f3eab51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504754"
---
# <span data-ttu-id="0db07-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0db07-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="0db07-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0db07-102">SYNOPSIS</span></span>
<span data-ttu-id="0db07-103">Erstellt einen neuen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0db07-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db07-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0db07-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <String> [-ImmutableId <String>]
 [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0db07-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0db07-105">DESCRIPTION</span></span>
<span data-ttu-id="0db07-106">Erstellt einen neuen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="0db07-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="0db07-107">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="0db07-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="0db07-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0db07-108">EXAMPLES</span></span>

### <span data-ttu-id="0db07-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0db07-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="0db07-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="0db07-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="0db07-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0db07-111">PARAMETERS</span></span>

### <span data-ttu-id="0db07-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0db07-112">-DisplayName</span></span>
<span data-ttu-id="0db07-113">Der Name, der im Adressbuch für den Benutzer angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0db07-113">The name to display in the address book for the user.</span></span>
<span data-ttu-id="0db07-114">Beispiel ' Alex Wu '</span><span class="sxs-lookup"><span data-stu-id="0db07-114">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="0db07-115">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="0db07-115">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="0db07-116">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern muss (wahr).</span><span class="sxs-lookup"><span data-stu-id="0db07-116">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="0db07-117">Standardverhalten ist (falsch), um das Kennwort bei der nächsten erfolgreichen Anmeldung nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0db07-117">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="0db07-118">-Unveränderlich</span><span class="sxs-lookup"><span data-stu-id="0db07-118">-ImmutableId</span></span>
<span data-ttu-id="0db07-119">Sie muss nur angegeben werden, wenn Sie eine Verbunddomäne für die Benutzerprinzipalnamen-Eigenschaft (User Principal Name, UPN) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0db07-119">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="0db07-120">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="0db07-120">-Password</span></span>
<span data-ttu-id="0db07-121">Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0db07-121">Password for the user.</span></span>
<span data-ttu-id="0db07-122">Das Kennwort muss den Komplexitätsanforderungen des Mandanten genügen.</span><span class="sxs-lookup"><span data-stu-id="0db07-122">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="0db07-123">Es wird empfohlen, ein sicheres Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0db07-123">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="0db07-124">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0db07-124">-UserPrincipalName</span></span>
<span data-ttu-id="0db07-125">Der Benutzerprinzipalname.</span><span class="sxs-lookup"><span data-stu-id="0db07-125">The user principal name.</span></span>
<span data-ttu-id="0db07-126">Beispiel: " someuser@contoso.com ".</span><span class="sxs-lookup"><span data-stu-id="0db07-126">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="0db07-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0db07-127">-Confirm</span></span>
<span data-ttu-id="0db07-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0db07-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db07-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db07-129">-WhatIf</span></span>
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

### <span data-ttu-id="0db07-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db07-130">-DefaultProfile</span></span>
<span data-ttu-id="0db07-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0db07-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0db07-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db07-132">CommonParameters</span></span>
<span data-ttu-id="0db07-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db07-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db07-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db07-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db07-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0db07-135">INPUTS</span></span>

## <span data-ttu-id="0db07-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0db07-136">OUTPUTS</span></span>

### <span data-ttu-id="0db07-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="0db07-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="0db07-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="0db07-138">NOTES</span></span>

## <span data-ttu-id="0db07-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0db07-139">RELATED LINKS</span></span>

[<span data-ttu-id="0db07-140">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0db07-140">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="0db07-141">Satz-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0db07-141">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="0db07-142">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0db07-142">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
