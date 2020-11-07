---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Remove-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 1c6f6a38c1811bdda32b60d4af1707c78eb7afd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662787"
---
# <span data-ttu-id="5e173-101">Remove-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5e173-101">Remove-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5e173-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e173-102">SYNOPSIS</span></span>
<span data-ttu-id="5e173-103">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e173-103">Deletes the security workspace setting for this subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e173-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e173-104">SYNTAX</span></span>

### <span data-ttu-id="5e173-105">SubscriptionLevelResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e173-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e173-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e173-106">ResourceId</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e173-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e173-107">InputObject</span></span>
```
Remove-AzureRmSecurityWorkspaceSetting -InputObject <PSRemoveWorkspaceSettingInputObject> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e173-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e173-108">DESCRIPTION</span></span>
<span data-ttu-id="5e173-109">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e173-109">Deletes the security workspace setting for this subscription.</span></span>
<span data-ttu-id="5e173-110">Mit dieser Aktion werden die neu installierten Sicherheits-Agents an den Standardarbeitsbereich dieses susbscription.</span><span class="sxs-lookup"><span data-stu-id="5e173-110">This action will make the newly installed security agents to report to the default workspace of this susbscription.</span></span>

## <span data-ttu-id="5e173-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e173-111">EXAMPLES</span></span>

### <span data-ttu-id="5e173-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e173-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmSecurityWorkspaceSetting -Name "default"
```

<span data-ttu-id="5e173-113">Löscht die Einstellungen für den Sicherheits Arbeitsbereich für dieses Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e173-113">Deletes the security workspace setting for this subscription.</span></span>

## <span data-ttu-id="5e173-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e173-114">PARAMETERS</span></span>

### <span data-ttu-id="5e173-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e173-115">-DefaultProfile</span></span>
<span data-ttu-id="5e173-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e173-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e173-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e173-117">-InputObject</span></span>
<span data-ttu-id="5e173-118">Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="5e173-118">Input Object.</span></span>

```yaml
Type: PSRemoveWorkspaceSettingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e173-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5e173-119">-Name</span></span>
<span data-ttu-id="5e173-120">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="5e173-120">Resource name.</span></span>

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

### <span data-ttu-id="5e173-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e173-121">-PassThru</span></span>
<span data-ttu-id="5e173-122">Gibt zurück, ob der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="5e173-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="5e173-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e173-123">-ResourceId</span></span>
<span data-ttu-id="5e173-124">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e173-124">Resource ID.</span></span>

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

### <span data-ttu-id="5e173-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e173-125">-Confirm</span></span>
<span data-ttu-id="5e173-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e173-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e173-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e173-127">-WhatIf</span></span>
<span data-ttu-id="5e173-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e173-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e173-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e173-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e173-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e173-130">CommonParameters</span></span>
<span data-ttu-id="5e173-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e173-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e173-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e173-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e173-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e173-133">INPUTS</span></span>

### <span data-ttu-id="5e173-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5e173-134">System.String</span></span>
<span data-ttu-id="5e173-135">Microsoft. Azure. Commands. Security. Cmdlets. WorkspaceSettings. PSRemoveWorkspaceSettingInputObject</span><span class="sxs-lookup"><span data-stu-id="5e173-135">Microsoft.Azure.Commands.Security.Cmdlets.WorkspaceSettings.PSRemoveWorkspaceSettingInputObject</span></span>

## <span data-ttu-id="5e173-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e173-136">OUTPUTS</span></span>

### <span data-ttu-id="5e173-137">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5e173-137">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5e173-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e173-138">NOTES</span></span>

## <span data-ttu-id="5e173-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e173-139">RELATED LINKS</span></span>
