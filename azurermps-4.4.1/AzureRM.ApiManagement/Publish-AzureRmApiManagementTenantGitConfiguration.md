---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Publish-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 2a867109bf44cd652eaf1d256d963796e06762cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479401"
---
# <span data-ttu-id="ff247-101">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff247-101">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="ff247-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff247-102">SYNOPSIS</span></span>
<span data-ttu-id="ff247-103">Veröffentlicht Änderungen aus einem git-Zweig in die Konfigurationsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ff247-103">Publishes changes from a Git branch to the configuration database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff247-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff247-104">SYNTAX</span></span>

```
Publish-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff247-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff247-105">DESCRIPTION</span></span>
<span data-ttu-id="ff247-106">Mit dem Cmdlet " **Publish-AzureRmApiManagementTenantGitConfiguration** " werden die Änderungen aus einer git-Verzweigung in die Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ff247-106">The **Publish-AzureRmApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="ff247-107">Sie können die Änderungen in einem git-Zweig auch ohne Veröffentlichung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ff247-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="ff247-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff247-108">EXAMPLES</span></span>

### <span data-ttu-id="ff247-109">Beispiel 1: Bereitstellen von git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="ff247-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="ff247-110">Mit diesem Befehl werden die Änderungen aus der angegebenen Verzweigung in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ff247-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="ff247-111">Beispiel 2: Überprüfen von git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="ff247-111">Example 2: Validate Git changes</span></span>
```
PS C:\>Publish-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="ff247-112">Mit diesem Befehl werden die Änderungen im git-Zweig für die Konfigurationsdatenbank überprüft.</span><span class="sxs-lookup"><span data-stu-id="ff247-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="ff247-113">Änderungen werden nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ff247-113">It does not publish changes.</span></span>

## <span data-ttu-id="ff247-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff247-114">PARAMETERS</span></span>

### <span data-ttu-id="ff247-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="ff247-115">-Branch</span></span>
<span data-ttu-id="ff247-116">Gibt den Namen des git-Zweigs an, aus dem dieses Cmdlet die Konfiguration in der Konfigurationsdatenbank bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ff247-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ff247-117">-Context</span></span>
<span data-ttu-id="ff247-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ff247-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ff247-119">-Force</span></span>
<span data-ttu-id="ff247-120">Gibt an, dass dieses Cmdlet Abonnements für Produkte löscht, die in diesem Update gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="ff247-120">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff247-121">-PassThru</span></span>
<span data-ttu-id="ff247-122">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ff247-122">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-123">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ff247-123">-ValidateOnly</span></span>
<span data-ttu-id="ff247-124">Gibt an, dass dieses Cmdlet die Änderungen in der angegebenen git-Verzweigung überprüft.</span><span class="sxs-lookup"><span data-stu-id="ff247-124">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="ff247-125">Sie wird nicht in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ff247-125">It does not publish to the configuration database.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff247-126">-Confirm</span></span>
<span data-ttu-id="ff247-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff247-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff247-128">-WhatIf</span></span>
<span data-ttu-id="ff247-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff247-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff247-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff247-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff247-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff247-131">-DefaultProfile</span></span>
<span data-ttu-id="ff247-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff247-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff247-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff247-133">CommonParameters</span></span>
<span data-ttu-id="ff247-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff247-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff247-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff247-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff247-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff247-136">INPUTS</span></span>

## <span data-ttu-id="ff247-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff247-137">OUTPUTS</span></span>

### <span data-ttu-id="ff247-138">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="ff247-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="ff247-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff247-139">NOTES</span></span>

## <span data-ttu-id="ff247-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff247-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff247-141">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff247-141">Save-AzureRmApiManagementTenantGitConfiguration</span></span>](./Save-AzureRmApiManagementTenantGitConfiguration.md)


