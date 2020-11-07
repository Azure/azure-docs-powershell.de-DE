---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADServicePrincipal.md
ms.openlocfilehash: 8bf47d9753d7cd8d97c14eb2ec1ac7c6384f7c1b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663428"
---
# <span data-ttu-id="ef8ff-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef8ff-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="ef8ff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ef8ff-103">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef8ff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef8ff-104">SYNTAX</span></span>

```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef8ff-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef8ff-105">DESCRIPTION</span></span>
<span data-ttu-id="ef8ff-106">Löscht den Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-106">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="ef8ff-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef8ff-107">EXAMPLES</span></span>

### <span data-ttu-id="ef8ff-108">Löschen Sie Aad-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-108">Delete AAD service principal.</span></span>
```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="ef8ff-109">Löscht den angegebenen Azure Active Directory-Dienstprinzipal.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-109">Deletes the given azure active directory service principal.</span></span>

## <span data-ttu-id="ef8ff-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef8ff-110">PARAMETERS</span></span>

### <span data-ttu-id="ef8ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef8ff-111">-DefaultProfile</span></span>
<span data-ttu-id="ef8ff-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ef8ff-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef8ff-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ef8ff-113">-Force</span></span>
<span data-ttu-id="ef8ff-114">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="ef8ff-114">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="ef8ff-115">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ef8ff-115">-ObjectId</span></span>
<span data-ttu-id="ef8ff-116">Die Objekt-ID des Dienst Prinzipals, der gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-116">The object id of the service principal to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef8ff-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef8ff-117">-PassThru</span></span>
<span data-ttu-id="ef8ff-118">Gibt, falls angegeben, den gelöschten Dienstprinzipal zurück.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-118">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="ef8ff-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ef8ff-119">-Confirm</span></span>
<span data-ttu-id="ef8ff-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef8ff-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef8ff-121">-WhatIf</span></span>
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

### <span data-ttu-id="ef8ff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef8ff-122">CommonParameters</span></span>
<span data-ttu-id="ef8ff-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef8ff-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef8ff-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef8ff-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef8ff-125">INPUTS</span></span>

### <span data-ttu-id="ef8ff-126">Keine</span><span class="sxs-lookup"><span data-stu-id="ef8ff-126">None</span></span>
<span data-ttu-id="ef8ff-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ef8ff-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef8ff-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef8ff-128">OUTPUTS</span></span>

### <span data-ttu-id="ef8ff-129">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef8ff-129">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="ef8ff-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef8ff-130">NOTES</span></span>
<span data-ttu-id="ef8ff-131">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ef8ff-131">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="ef8ff-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef8ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="ef8ff-133">Neu – AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef8ff-133">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="ef8ff-134">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef8ff-134">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="ef8ff-135">Satz-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="ef8ff-135">Set-AzureRmADServicePrincipal</span></span>](./Set-AzureRmADServicePrincipal.md)

[<span data-ttu-id="ef8ff-136">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ef8ff-136">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="ef8ff-137">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ef8ff-137">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
