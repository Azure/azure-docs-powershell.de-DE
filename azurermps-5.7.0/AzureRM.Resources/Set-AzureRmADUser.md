---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476606"
---
# <span data-ttu-id="e9fd3-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="e9fd3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fd3-103">Aktualisiert einen vorhandenen Active Directory-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9fd3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9fd3-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9fd3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="e9fd3-106">Aktualisiert einen vorhandenen Active Directory-Benutzer (Firmen-oder Schulkonto, auch bekannt als org-ID).</span><span class="sxs-lookup"><span data-stu-id="e9fd3-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="e9fd3-107">Weitere Informationen: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="e9fd3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9fd3-108">EXAMPLES</span></span>

### <span data-ttu-id="e9fd3-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e9fd3-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e9fd3-110">{{Add Example Description here}}</span><span class="sxs-lookup"><span data-stu-id="e9fd3-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="e9fd3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9fd3-111">PARAMETERS</span></span>

### <span data-ttu-id="e9fd3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fd3-112">-DefaultProfile</span></span>
<span data-ttu-id="e9fd3-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e9fd3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e9fd3-114">-DisplayName</span></span>
<span data-ttu-id="e9fd3-115">Der neue Name, der im Adressbuch des Benutzers angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="e9fd3-116">Beispiel – 'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-116">Example-'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="e9fd3-117">-EnableAccount</span></span>
<span data-ttu-id="e9fd3-118">True zum Aktivieren des Kontos; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="e9fd3-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="e9fd3-120">Sie muss nur angegeben werden, wenn Sie das Kennwort aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="e9fd3-121">Andernfalls wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="e9fd3-122">Sie muss angegeben werden, wenn der Benutzer das Kennwort bei der nächsten erfolgreichen Anmeldung ändern muss (wahr).</span><span class="sxs-lookup"><span data-stu-id="e9fd3-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="e9fd3-123">Standardverhalten ist (falsch), um das Kennwort bei der nächsten erfolgreichen Anmeldung nicht zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-124">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="e9fd3-124">-Password</span></span>
<span data-ttu-id="e9fd3-125">Neues Kennwort für den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-125">New password for the user.</span></span>
<span data-ttu-id="e9fd3-126">Das Kennwort muss den Komplexitätsanforderungen des Mandanten genügen.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="e9fd3-127">Es wird empfohlen, ein sicheres Kennwort festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="e9fd3-128">-UPNOrObjectId</span></span>
<span data-ttu-id="e9fd3-129">Der Benutzerprinzipalname (z. b. ' someuser@contoso.com ') oder die ObjectID des Benutzers, für den die Eigenschaften aktualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="e9fd3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9fd3-130">-Confirm</span></span>
<span data-ttu-id="e9fd3-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9fd3-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fd3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fd3-133">CommonParameters</span></span>
<span data-ttu-id="e9fd3-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fd3-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9fd3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fd3-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9fd3-136">INPUTS</span></span>

### <span data-ttu-id="e9fd3-137">Keine</span><span class="sxs-lookup"><span data-stu-id="e9fd3-137">None</span></span>
<span data-ttu-id="e9fd3-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e9fd3-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e9fd3-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9fd3-139">OUTPUTS</span></span>

### <span data-ttu-id="e9fd3-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="e9fd3-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9fd3-141">NOTES</span></span>

## <span data-ttu-id="e9fd3-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9fd3-142">RELATED LINKS</span></span>

[<span data-ttu-id="e9fd3-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="e9fd3-144">Neu – AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="e9fd3-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e9fd3-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

