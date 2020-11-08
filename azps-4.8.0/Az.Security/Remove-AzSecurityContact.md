---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: b4cbecd2e29a0b70c7e62194df2364b22b33b462
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174174"
---
# <span data-ttu-id="c5445-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c5445-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="c5445-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5445-102">SYNOPSIS</span></span>
<span data-ttu-id="c5445-103">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="c5445-103">Deletes a security contact.</span></span>

## <span data-ttu-id="c5445-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5445-104">SYNTAX</span></span>

### <span data-ttu-id="c5445-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5445-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5445-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5445-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5445-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c5445-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5445-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5445-108">DESCRIPTION</span></span>
<span data-ttu-id="c5445-109">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="c5445-109">Deletes a security contact.</span></span>

## <span data-ttu-id="c5445-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5445-110">EXAMPLES</span></span>

### <span data-ttu-id="c5445-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5445-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="c5445-112">Löscht den Sicherheitskontakt "Installation1"</span><span class="sxs-lookup"><span data-stu-id="c5445-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="c5445-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5445-113">PARAMETERS</span></span>

### <span data-ttu-id="c5445-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5445-114">-DefaultProfile</span></span>
<span data-ttu-id="c5445-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c5445-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5445-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c5445-116">-InputObject</span></span>
<span data-ttu-id="c5445-117">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="c5445-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5445-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c5445-118">-Name</span></span>
<span data-ttu-id="c5445-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="c5445-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5445-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5445-120">-PassThru</span></span>
<span data-ttu-id="c5445-121">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c5445-121">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5445-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5445-122">-ResourceId</span></span>
<span data-ttu-id="c5445-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c5445-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5445-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c5445-124">-Confirm</span></span>
<span data-ttu-id="c5445-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5445-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5445-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5445-126">-WhatIf</span></span>
<span data-ttu-id="c5445-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5445-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5445-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5445-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5445-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5445-129">CommonParameters</span></span>
<span data-ttu-id="c5445-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5445-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5445-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5445-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5445-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5445-132">INPUTS</span></span>

### <span data-ttu-id="c5445-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c5445-133">System.String</span></span>

### <span data-ttu-id="c5445-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="c5445-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="c5445-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5445-135">OUTPUTS</span></span>

### <span data-ttu-id="c5445-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c5445-136">System.Boolean</span></span>

## <span data-ttu-id="c5445-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5445-137">NOTES</span></span>

## <span data-ttu-id="c5445-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5445-138">RELATED LINKS</span></span>
