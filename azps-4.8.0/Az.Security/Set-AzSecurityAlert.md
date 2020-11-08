---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: 0555b86b6e5240adfc43bc52153bf14d7612be1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165590"
---
# <span data-ttu-id="a89a3-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a89a3-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="a89a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a89a3-102">SYNOPSIS</span></span>
<span data-ttu-id="a89a3-103">Aktualisiert einen Sicherheits Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="a89a3-103">Updates a security alert state.</span></span>

## <span data-ttu-id="a89a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a89a3-104">SYNTAX</span></span>

### <span data-ttu-id="a89a3-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a89a3-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89a3-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a89a3-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89a3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a89a3-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89a3-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="a89a3-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a89a3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a89a3-109">DESCRIPTION</span></span>
<span data-ttu-id="a89a3-110">Legt einen Sicherheits Warnungsstatus fest.</span><span class="sxs-lookup"><span data-stu-id="a89a3-110">Sets a security alert state.</span></span>

## <span data-ttu-id="a89a3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a89a3-111">EXAMPLES</span></span>

### <span data-ttu-id="a89a3-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a89a3-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="a89a3-113">Gibt eine ausgelöste Sicherheitswarnung aus.</span><span class="sxs-lookup"><span data-stu-id="a89a3-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="a89a3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a89a3-114">PARAMETERS</span></span>

### <span data-ttu-id="a89a3-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="a89a3-115">-ActionType</span></span>
<span data-ttu-id="a89a3-116">Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="a89a3-116">Action Type.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89a3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89a3-117">-DefaultProfile</span></span>
<span data-ttu-id="a89a3-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a89a3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a89a3-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a89a3-119">-InputObject</span></span>
<span data-ttu-id="a89a3-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="a89a3-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89a3-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="a89a3-121">-Location</span></span>
<span data-ttu-id="a89a3-122">Lage.</span><span class="sxs-lookup"><span data-stu-id="a89a3-122">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89a3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a89a3-123">-Name</span></span>
<span data-ttu-id="a89a3-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a89a3-124">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89a3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a89a3-125">-PassThru</span></span>
<span data-ttu-id="a89a3-126">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a89a3-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="a89a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="a89a3-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a89a3-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89a3-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a89a3-129">-ResourceId</span></span>
<span data-ttu-id="a89a3-130">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a89a3-130">Resource ID.</span></span>

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

### <span data-ttu-id="a89a3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a89a3-131">-Confirm</span></span>
<span data-ttu-id="a89a3-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a89a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a89a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89a3-133">-WhatIf</span></span>
<span data-ttu-id="a89a3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a89a3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a89a3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a89a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a89a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89a3-136">CommonParameters</span></span>
<span data-ttu-id="a89a3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a89a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89a3-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a89a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89a3-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a89a3-139">INPUTS</span></span>

### <span data-ttu-id="a89a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a89a3-140">System.String</span></span>

### <span data-ttu-id="a89a3-141">Microsoft. Azure. Commands. Security. Models. alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="a89a3-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="a89a3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a89a3-142">OUTPUTS</span></span>

### <span data-ttu-id="a89a3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a89a3-143">System.Boolean</span></span>

## <span data-ttu-id="a89a3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a89a3-144">NOTES</span></span>

## <span data-ttu-id="a89a3-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a89a3-145">RELATED LINKS</span></span>
