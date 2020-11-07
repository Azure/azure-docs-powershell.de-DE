---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 9a0a7252b0ad20f647ef39094ff632302d5b22cf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663431"
---
# <span data-ttu-id="4b60b-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b60b-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="4b60b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4b60b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b60b-103">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4b60b-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b60b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b60b-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b60b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b60b-105">DESCRIPTION</span></span>
<span data-ttu-id="4b60b-106">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4b60b-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4b60b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4b60b-107">EXAMPLES</span></span>

### <span data-ttu-id="4b60b-108">Löschen Sie Aad-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4b60b-108">Delete AAD application.</span></span>
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="4b60b-109">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4b60b-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="4b60b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b60b-110">PARAMETERS</span></span>

### <span data-ttu-id="4b60b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b60b-111">-DefaultProfile</span></span>
<span data-ttu-id="4b60b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4b60b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b60b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4b60b-113">-Force</span></span>
<span data-ttu-id="4b60b-114">Wechseln Sie, um eine Anwendung ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="4b60b-114">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="4b60b-115">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="4b60b-115">-ObjectId</span></span>
<span data-ttu-id="4b60b-116">Die Objekt-ID der zu löschenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4b60b-116">The object id of the application to delete.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b60b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4b60b-117">-Confirm</span></span>
<span data-ttu-id="4b60b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4b60b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b60b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b60b-119">-WhatIf</span></span>
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

### <span data-ttu-id="4b60b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b60b-120">CommonParameters</span></span>
<span data-ttu-id="4b60b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b60b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b60b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b60b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b60b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4b60b-123">INPUTS</span></span>

### <span data-ttu-id="4b60b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="4b60b-124">None</span></span>
<span data-ttu-id="4b60b-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4b60b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b60b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4b60b-126">OUTPUTS</span></span>

## <span data-ttu-id="4b60b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="4b60b-127">NOTES</span></span>
<span data-ttu-id="4b60b-128">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="4b60b-128">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4b60b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4b60b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b60b-130">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b60b-130">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="4b60b-131">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b60b-131">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="4b60b-132">Satz-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="4b60b-132">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="4b60b-133">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="4b60b-133">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

