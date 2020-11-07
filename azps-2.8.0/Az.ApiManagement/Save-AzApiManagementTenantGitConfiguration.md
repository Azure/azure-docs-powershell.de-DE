---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 1caabfbf5c3139f27b44f8ccad3612eb34f36fd4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658166"
---
# <span data-ttu-id="4289c-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4289c-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="4289c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4289c-102">SYNOPSIS</span></span>
<span data-ttu-id="4289c-103">Speichert Änderungen, indem ein Commit für die aktuelle Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4289c-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="4289c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4289c-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4289c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4289c-105">DESCRIPTION</span></span>
<span data-ttu-id="4289c-106">Das Cmdlet **Save-AzApiManagementTenantGitConfiguration** speichert die Änderungen durch Erstellen eines Commits, der den aktuellen Konfigurations-Snapshot für eine Verzweigung im Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="4289c-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="4289c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4289c-107">EXAMPLES</span></span>

### <span data-ttu-id="4289c-108">Beispiel 1: Speichern von Änderungen an der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="4289c-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="4289c-109">Dieser Befehl speichert die Änderungen, indem ein Commit mit dem aktuellen Konfigurations-Snapshot für die angegebene Verzweigung im Repository erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4289c-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="4289c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4289c-110">PARAMETERS</span></span>

### <span data-ttu-id="4289c-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="4289c-111">-Branch</span></span>
<span data-ttu-id="4289c-112">Gibt den Namen der git-Verzweigung an, in der der aktuelle Konfigurations-Snapshot übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4289c-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="4289c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4289c-113">-Context</span></span>
<span data-ttu-id="4289c-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4289c-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4289c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4289c-115">-DefaultProfile</span></span>
<span data-ttu-id="4289c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4289c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4289c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4289c-117">-Force</span></span>
<span data-ttu-id="4289c-118">Gibt an, dass dieses Cmdlet die aktuelle Konfigurationsdatenbank an das git-Repository übergibt, selbst wenn das git-Repository neuere Änderungen enthält, die überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="4289c-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="4289c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4289c-119">-PassThru</span></span>
<span data-ttu-id="4289c-120">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="4289c-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="4289c-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4289c-121">-Confirm</span></span>
<span data-ttu-id="4289c-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4289c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4289c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4289c-123">-WhatIf</span></span>
<span data-ttu-id="4289c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4289c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4289c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4289c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4289c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4289c-126">CommonParameters</span></span>
<span data-ttu-id="4289c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4289c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4289c-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4289c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4289c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4289c-129">INPUTS</span></span>

### <span data-ttu-id="4289c-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4289c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4289c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4289c-131">System.String</span></span>

### <span data-ttu-id="4289c-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4289c-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4289c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4289c-133">OUTPUTS</span></span>

### <span data-ttu-id="4289c-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="4289c-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="4289c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="4289c-135">NOTES</span></span>

## <span data-ttu-id="4289c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4289c-136">RELATED LINKS</span></span>

[<span data-ttu-id="4289c-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="4289c-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


