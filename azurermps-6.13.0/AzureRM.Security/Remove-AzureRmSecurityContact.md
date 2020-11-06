---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityContact.md
ms.openlocfilehash: 8c2f6a45bb483109b61be47de3013f3ccb4d5c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501070"
---
# <span data-ttu-id="f7f2b-101">Remove-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="f7f2b-101">Remove-AzureRmSecurityContact</span></span>

## <span data-ttu-id="f7f2b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f2b-103">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-103">Deletes a security contact.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f2b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7f2b-104">SYNTAX</span></span>

### <span data-ttu-id="f7f2b-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7f2b-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f2b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f2b-106">ResourceId</span></span>
```
Remove-AzureRmSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f2b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f2b-107">InputObject</span></span>
```
Remove-AzureRmSecurityContact -InputObject <PSRemoveSecurityContactInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f2b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="f7f2b-109">Löscht einen Sicherheitskontakt.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-109">Deletes a security contact.</span></span>

## <span data-ttu-id="f7f2b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7f2b-110">EXAMPLES</span></span>

### <span data-ttu-id="f7f2b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7f2b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityContact -Name "default1"
```

<span data-ttu-id="f7f2b-112">Löscht den Sicherheitskontakt "Installation1"</span><span class="sxs-lookup"><span data-stu-id="f7f2b-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="f7f2b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7f2b-113">PARAMETERS</span></span>

### <span data-ttu-id="f7f2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f2b-114">-DefaultProfile</span></span>
<span data-ttu-id="f7f2b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f2b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7f2b-116">-InputObject</span></span>
<span data-ttu-id="f7f2b-117">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-117">Input Object.</span></span>

```yaml
Type: PSRemoveSecurityContactInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f2b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f2b-118">-Name</span></span>
<span data-ttu-id="f7f2b-119">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="f7f2b-119">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f2b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7f2b-120">-PassThru</span></span>
<span data-ttu-id="f7f2b-121">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-121">Return whether the operation was successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f2b-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7f2b-122">-ResourceId</span></span>
<span data-ttu-id="f7f2b-123">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-123">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f2b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7f2b-124">-Confirm</span></span>
<span data-ttu-id="f7f2b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f2b-126">-WhatIf</span></span>
<span data-ttu-id="f7f2b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f2b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f2b-129">CommonParameters</span></span>
<span data-ttu-id="f7f2b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f2b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f2b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f2b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7f2b-132">INPUTS</span></span>

### <span data-ttu-id="f7f2b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f2b-133">System.String</span></span>
<span data-ttu-id="f7f2b-134">Microsoft. Azure. Commands. Security. Cmdlets. SecurityContacts. PSRemoveSecurityContactInputObject</span><span class="sxs-lookup"><span data-stu-id="f7f2b-134">Microsoft.Azure.Commands.Security.Cmdlets.SecurityContacts.PSRemoveSecurityContactInputObject</span></span>

## <span data-ttu-id="f7f2b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7f2b-135">OUTPUTS</span></span>

### <span data-ttu-id="f7f2b-136">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="f7f2b-136">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="f7f2b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7f2b-137">NOTES</span></span>

## <span data-ttu-id="f7f2b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7f2b-138">RELATED LINKS</span></span>
