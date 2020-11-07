---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662401"
---
# <span data-ttu-id="f3779-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f3779-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="f3779-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3779-102">SYNOPSIS</span></span>
<span data-ttu-id="f3779-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f3779-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3779-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3779-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3779-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3779-105">DESCRIPTION</span></span>
<span data-ttu-id="f3779-106">Aktualisiert einen vorhandenen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="f3779-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="f3779-107">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="f3779-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="f3779-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3779-108">EXAMPLES</span></span>

### <span data-ttu-id="f3779-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3779-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f3779-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="f3779-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="f3779-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3779-111">PARAMETERS</span></span>

### <span data-ttu-id="f3779-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3779-112">-DisplayName</span></span>
<span data-ttu-id="f3779-113">Der neue Name, der im Adressbuch des Benutzers angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3779-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="f3779-114">Beispiel – 'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="f3779-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="f3779-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="f3779-115">-EnableAccount</span></span>
<span data-ttu-id="f3779-116">True zum Aktivieren des Kontos; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="f3779-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3779-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="f3779-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="f3779-118">Sie muss nur angegeben werden, wenn Sie das Kennwort aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f3779-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="f3779-119">Andernfalls wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="f3779-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="f3779-120">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern muss (wahr).</span><span class="sxs-lookup"><span data-stu-id="f3779-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="f3779-121">Standardverhalten ist (falsch), um das Kennwort bei der nächsten erfolgreichen Anmeldung nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f3779-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="f3779-122">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="f3779-122">-Password</span></span>
<span data-ttu-id="f3779-123">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f3779-123">New password for the user.</span></span>
<span data-ttu-id="f3779-124">Das Kennwort muss den Komplexitätsanforderungen des Mandanten genügen.</span><span class="sxs-lookup"><span data-stu-id="f3779-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="f3779-125">Es wird empfohlen, ein sicheres Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f3779-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="f3779-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="f3779-126">-UPNOrObjectId</span></span>
<span data-ttu-id="f3779-127">Der Benutzerprinzipalname (z. b. ' someuser@contoso.com ') oder die ObjectID des Benutzers, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f3779-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="f3779-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3779-128">-Confirm</span></span>
<span data-ttu-id="f3779-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3779-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3779-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3779-130">-WhatIf</span></span>
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

### <span data-ttu-id="f3779-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3779-131">-DefaultProfile</span></span>
<span data-ttu-id="f3779-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f3779-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3779-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3779-133">CommonParameters</span></span>
<span data-ttu-id="f3779-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3779-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3779-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3779-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3779-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3779-136">INPUTS</span></span>

## <span data-ttu-id="f3779-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3779-137">OUTPUTS</span></span>

### <span data-ttu-id="f3779-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="f3779-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="f3779-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3779-139">NOTES</span></span>

## <span data-ttu-id="f3779-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3779-140">RELATED LINKS</span></span>

[<span data-ttu-id="f3779-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f3779-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="f3779-142">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f3779-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="f3779-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="f3779-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

