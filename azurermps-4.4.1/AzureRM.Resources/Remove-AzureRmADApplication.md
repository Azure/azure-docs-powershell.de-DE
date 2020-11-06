---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADApplication.md
ms.openlocfilehash: 0b0b560a97e223820a3a73ce036a5d7599df9a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500718"
---
# <span data-ttu-id="a826b-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a826b-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="a826b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a826b-102">SYNOPSIS</span></span>
<span data-ttu-id="a826b-103">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a826b-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a826b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a826b-104">SYNTAX</span></span>

```
Remove-AzureRmADApplication -ObjectId <Guid> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a826b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a826b-105">DESCRIPTION</span></span>
<span data-ttu-id="a826b-106">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a826b-106">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a826b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a826b-107">EXAMPLES</span></span>

### <span data-ttu-id="a826b-108">--------------------------Löschen Aad-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a826b-108">--------------------------  Delete AAD application.</span></span>  --------------------------
```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 -Force
```

<span data-ttu-id="a826b-109">Löscht die Azure Active Directory-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a826b-109">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="a826b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a826b-110">PARAMETERS</span></span>

### <span data-ttu-id="a826b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a826b-111">-Force</span></span>
<span data-ttu-id="a826b-112">Wechseln Sie, um eine Anwendung ohne Bestätigung zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a826b-112">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="a826b-113">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a826b-113">-ObjectId</span></span>
<span data-ttu-id="a826b-114">Die Objekt-ID der zu löschenden Anwendung.</span><span class="sxs-lookup"><span data-stu-id="a826b-114">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a826b-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a826b-115">-Confirm</span></span>
<span data-ttu-id="a826b-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a826b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a826b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a826b-117">-WhatIf</span></span>
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

### <span data-ttu-id="a826b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a826b-118">-DefaultProfile</span></span>
<span data-ttu-id="a826b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a826b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a826b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a826b-120">CommonParameters</span></span>
<span data-ttu-id="a826b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a826b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a826b-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a826b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a826b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a826b-123">INPUTS</span></span>

## <span data-ttu-id="a826b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a826b-124">OUTPUTS</span></span>

## <span data-ttu-id="a826b-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a826b-125">NOTES</span></span>
<span data-ttu-id="a826b-126">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="a826b-126">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="a826b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a826b-127">RELATED LINKS</span></span>

[<span data-ttu-id="a826b-128">Neu – AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a826b-128">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="a826b-129">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a826b-129">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="a826b-130">Satz-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="a826b-130">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="a826b-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a826b-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

