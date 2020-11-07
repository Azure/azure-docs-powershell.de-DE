---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAlert.md
ms.openlocfilehash: c9ed93f1a55f7c8cc52bef68d306f7d246d595a2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659438"
---
# <span data-ttu-id="0e477-101">Set-AzSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="0e477-101">Set-AzSecurityAlert</span></span>

## <span data-ttu-id="0e477-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e477-102">SYNOPSIS</span></span>
<span data-ttu-id="0e477-103">Aktualisiert einen Sicherheits Warnungszustand.</span><span class="sxs-lookup"><span data-stu-id="0e477-103">Updates a security alert state.</span></span>

## <span data-ttu-id="0e477-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e477-104">SYNTAX</span></span>

### <span data-ttu-id="0e477-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e477-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAlert -Location <String> -Name <String> -ActionType <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e477-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0e477-106">ResourceGroupLevelResource</span></span>
```
Set-AzSecurityAlert -ResourceGroupName <String> -Location <String> -Name <String> -ActionType <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e477-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e477-107">ResourceId</span></span>
```
Set-AzSecurityAlert -ActionType <String> -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e477-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="0e477-108">InputObject</span></span>
```
Set-AzSecurityAlert [-ActionType <String>] -InputObject <PSSecurityAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e477-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e477-109">DESCRIPTION</span></span>
<span data-ttu-id="0e477-110">Legt einen Sicherheits Warnungsstatus fest.</span><span class="sxs-lookup"><span data-stu-id="0e477-110">Sets a security alert state.</span></span>

## <span data-ttu-id="0e477-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e477-111">EXAMPLES</span></span>

### <span data-ttu-id="0e477-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e477-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAlert -Location "centralus" -ResourceGroupName "RSG" -Name "2518710774294070750_FFF23C70-80EF-4A8B-9122-507B0EA8DFFF" -ActionType Dismiss
```

<span data-ttu-id="0e477-113">Gibt eine ausgelöste Sicherheitswarnung aus.</span><span class="sxs-lookup"><span data-stu-id="0e477-113">Dismisses a security alert that was raised.</span></span>

## <span data-ttu-id="0e477-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e477-114">PARAMETERS</span></span>

### <span data-ttu-id="0e477-115">-ActionType</span><span class="sxs-lookup"><span data-stu-id="0e477-115">-ActionType</span></span>
<span data-ttu-id="0e477-116">Aktionstyp</span><span class="sxs-lookup"><span data-stu-id="0e477-116">Action Type.</span></span>

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

### <span data-ttu-id="0e477-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e477-117">-DefaultProfile</span></span>
<span data-ttu-id="0e477-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e477-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e477-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0e477-119">-InputObject</span></span>
<span data-ttu-id="0e477-120">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="0e477-120">Input Object.</span></span>

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

### <span data-ttu-id="0e477-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="0e477-121">-Location</span></span>
<span data-ttu-id="0e477-122">Lage.</span><span class="sxs-lookup"><span data-stu-id="0e477-122">Location.</span></span>

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

### <span data-ttu-id="0e477-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0e477-123">-Name</span></span>
<span data-ttu-id="0e477-124">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="0e477-124">Resource name.</span></span>

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

### <span data-ttu-id="0e477-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e477-125">-PassThru</span></span>
<span data-ttu-id="0e477-126">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="0e477-126">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="0e477-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e477-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e477-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0e477-128">Resource group name.</span></span>

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

### <span data-ttu-id="0e477-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0e477-129">-ResourceId</span></span>
<span data-ttu-id="0e477-130">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0e477-130">Resource ID.</span></span>

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

### <span data-ttu-id="0e477-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0e477-131">-Confirm</span></span>
<span data-ttu-id="0e477-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0e477-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e477-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e477-133">-WhatIf</span></span>
<span data-ttu-id="0e477-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0e477-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e477-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e477-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e477-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e477-136">CommonParameters</span></span>
<span data-ttu-id="0e477-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e477-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e477-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e477-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e477-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e477-139">INPUTS</span></span>

### <span data-ttu-id="0e477-140">System. String</span><span class="sxs-lookup"><span data-stu-id="0e477-140">System.String</span></span>

### <span data-ttu-id="0e477-141">Microsoft. Azure. Commands. Security. Models. alerts. PSSecurityAlert</span><span class="sxs-lookup"><span data-stu-id="0e477-141">Microsoft.Azure.Commands.Security.Models.Alerts.PSSecurityAlert</span></span>

## <span data-ttu-id="0e477-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e477-142">OUTPUTS</span></span>

### <span data-ttu-id="0e477-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e477-143">System.Boolean</span></span>

## <span data-ttu-id="0e477-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e477-144">NOTES</span></span>

## <span data-ttu-id="0e477-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e477-145">RELATED LINKS</span></span>
