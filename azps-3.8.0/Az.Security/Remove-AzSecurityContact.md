---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: ed4afca4d422245be721c7b50d45ecaab45b5c81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996286"
---
# <span data-ttu-id="274d7-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="274d7-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="274d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="274d7-102">SYNOPSIS</span></span>
<span data-ttu-id="274d7-103">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="274d7-103">Deletes a security contact.</span></span>

## <span data-ttu-id="274d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="274d7-104">SYNTAX</span></span>

### <span data-ttu-id="274d7-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="274d7-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="274d7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="274d7-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="274d7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="274d7-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="274d7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="274d7-108">DESCRIPTION</span></span>
<span data-ttu-id="274d7-109">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="274d7-109">Deletes a security contact.</span></span>

## <span data-ttu-id="274d7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="274d7-110">EXAMPLES</span></span>

### <span data-ttu-id="274d7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="274d7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="274d7-112">Löscht den Sicherheitskontakt "Installation1"</span><span class="sxs-lookup"><span data-stu-id="274d7-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="274d7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="274d7-113">PARAMETERS</span></span>

### <span data-ttu-id="274d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274d7-114">-DefaultProfile</span></span>
<span data-ttu-id="274d7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="274d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="274d7-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="274d7-116">-InputObject</span></span>
<span data-ttu-id="274d7-117">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="274d7-117">Input Object.</span></span>

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

### <span data-ttu-id="274d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="274d7-118">-Name</span></span>
<span data-ttu-id="274d7-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="274d7-119">Resource name.</span></span>

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

### <span data-ttu-id="274d7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="274d7-120">-PassThru</span></span>
<span data-ttu-id="274d7-121">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="274d7-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="274d7-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="274d7-122">-ResourceId</span></span>
<span data-ttu-id="274d7-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="274d7-123">Resource ID.</span></span>

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

### <span data-ttu-id="274d7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="274d7-124">-Confirm</span></span>
<span data-ttu-id="274d7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="274d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="274d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="274d7-126">-WhatIf</span></span>
<span data-ttu-id="274d7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="274d7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="274d7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="274d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="274d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274d7-129">CommonParameters</span></span>
<span data-ttu-id="274d7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="274d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274d7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274d7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="274d7-132">INPUTS</span></span>

### <span data-ttu-id="274d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="274d7-133">System.String</span></span>

### <span data-ttu-id="274d7-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="274d7-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="274d7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="274d7-135">OUTPUTS</span></span>

### <span data-ttu-id="274d7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="274d7-136">System.Boolean</span></span>

## <span data-ttu-id="274d7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="274d7-137">NOTES</span></span>

## <span data-ttu-id="274d7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="274d7-138">RELATED LINKS</span></span>
