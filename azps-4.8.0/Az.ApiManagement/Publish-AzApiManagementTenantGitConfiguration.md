---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 4783305F-5619-446A-A6DF-BD1E56739A2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/publish-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Publish-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 288bb02ffad3669615df3535aec7f691162daa2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173967"
---
# <span data-ttu-id="8149d-101">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="8149d-101">Publish-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="8149d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8149d-102">SYNOPSIS</span></span>
<span data-ttu-id="8149d-103">Veröffentlicht Änderungen aus einem git-Zweig in die Konfigurationsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8149d-103">Publishes changes from a Git branch to the configuration database.</span></span>

## <span data-ttu-id="8149d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8149d-104">SYNTAX</span></span>

```
Publish-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-ValidateOnly] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8149d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8149d-105">DESCRIPTION</span></span>
<span data-ttu-id="8149d-106">Mit dem Cmdlet " **Publish-AzApiManagementTenantGitConfiguration** " werden die Änderungen aus einer git-Verzweigung in die Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8149d-106">The **Publish-AzApiManagementTenantGitConfiguration** cmdlet publishes the changes from a Git branch to the configuration database.</span></span>
<span data-ttu-id="8149d-107">Sie können die Änderungen in einem git-Zweig auch ohne Veröffentlichung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8149d-107">You can alternatively validate the changes in a Git branch without publishing.</span></span>

## <span data-ttu-id="8149d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8149d-108">EXAMPLES</span></span>

### <span data-ttu-id="8149d-109">Beispiel 1: Bereitstellen von git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="8149d-109">Example 1: Deploy Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="8149d-110">Mit diesem Befehl werden die Änderungen aus der angegebenen Verzweigung in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8149d-110">This command publishes the changes from the specified branch to the configuration database.</span></span>

### <span data-ttu-id="8149d-111">Beispiel 2: Überprüfen von git-Änderungen</span><span class="sxs-lookup"><span data-stu-id="8149d-111">Example 2: Validate Git changes</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Publish-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -ValidateOnly -PassThru
```

<span data-ttu-id="8149d-112">Mit diesem Befehl werden die Änderungen im git-Zweig für die Konfigurationsdatenbank überprüft.</span><span class="sxs-lookup"><span data-stu-id="8149d-112">This command validates the changes in the Git branch against the configuration database.</span></span>
<span data-ttu-id="8149d-113">Änderungen werden nicht veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8149d-113">It does not publish changes.</span></span>

## <span data-ttu-id="8149d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8149d-114">PARAMETERS</span></span>

### <span data-ttu-id="8149d-115">-Branch</span><span class="sxs-lookup"><span data-stu-id="8149d-115">-Branch</span></span>
<span data-ttu-id="8149d-116">Gibt den Namen des git-Zweigs an, aus dem dieses Cmdlet die Konfiguration in der Konfigurationsdatenbank bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8149d-116">Specifies the name of the Git branch from which this cmdlet deploys the configuration to the configuration database.</span></span>

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

### <span data-ttu-id="8149d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8149d-117">-Context</span></span>
<span data-ttu-id="8149d-118">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8149d-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8149d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8149d-119">-DefaultProfile</span></span>
<span data-ttu-id="8149d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8149d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8149d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8149d-121">-Force</span></span>
<span data-ttu-id="8149d-122">Gibt an, dass dieses Cmdlet Abonnements für Produkte löscht, die in diesem Update gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="8149d-122">Indicates that this cmdlet deletes subscriptions to products that are deleted in this update.</span></span>

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

### <span data-ttu-id="8149d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8149d-123">-PassThru</span></span>
<span data-ttu-id="8149d-124">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8149d-124">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="8149d-125">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8149d-125">-ValidateOnly</span></span>
<span data-ttu-id="8149d-126">Gibt an, dass dieses Cmdlet die Änderungen in der angegebenen git-Verzweigung überprüft.</span><span class="sxs-lookup"><span data-stu-id="8149d-126">Indicates that this cmdlet validates the changes in the specified Git branch.</span></span>
<span data-ttu-id="8149d-127">Sie wird nicht in der Konfigurationsdatenbank veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="8149d-127">It does not publish to the configuration database.</span></span>

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

### <span data-ttu-id="8149d-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8149d-128">-Confirm</span></span>
<span data-ttu-id="8149d-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8149d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8149d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8149d-130">-WhatIf</span></span>
<span data-ttu-id="8149d-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8149d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8149d-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8149d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8149d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8149d-133">CommonParameters</span></span>
<span data-ttu-id="8149d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8149d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8149d-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8149d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8149d-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8149d-136">INPUTS</span></span>

### <span data-ttu-id="8149d-137">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8149d-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8149d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8149d-138">System.String</span></span>

### <span data-ttu-id="8149d-139">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8149d-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8149d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8149d-140">OUTPUTS</span></span>

### <span data-ttu-id="8149d-141">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="8149d-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="8149d-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8149d-142">NOTES</span></span>

## <span data-ttu-id="8149d-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8149d-143">RELATED LINKS</span></span>

[<span data-ttu-id="8149d-144">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="8149d-144">Save-AzApiManagementTenantGitConfiguration</span></span>](./Save-AzApiManagementTenantGitConfiguration.md)


