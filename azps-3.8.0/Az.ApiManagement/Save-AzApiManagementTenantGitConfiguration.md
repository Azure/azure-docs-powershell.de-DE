---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/save-azapimanagementtenantgitconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Save-AzApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 3995506c302d2993623f12fcb7e6e2b9f96fd208
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996830"
---
# <span data-ttu-id="80c39-101">Save-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="80c39-101">Save-AzApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="80c39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80c39-102">SYNOPSIS</span></span>
<span data-ttu-id="80c39-103">Speichert Änderungen, indem ein Commit für die aktuelle Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="80c39-103">Saves changes by creating a commit for current configuration.</span></span>

## <span data-ttu-id="80c39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c39-104">SYNTAX</span></span>

```
Save-AzApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80c39-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80c39-105">DESCRIPTION</span></span>
<span data-ttu-id="80c39-106">Das Cmdlet **Save-AzApiManagementTenantGitConfiguration** speichert die Änderungen durch Erstellen eines Commits, der den aktuellen Konfigurations-Snapshot für eine Verzweigung im Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="80c39-106">The **Save-AzApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="80c39-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80c39-107">EXAMPLES</span></span>

### <span data-ttu-id="80c39-108">Beispiel 1: Speichern von Änderungen an der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="80c39-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Save-AzApiManagementTenantGitConfiguration -Context $apimContext -Branch 'master' -PassThru
```

<span data-ttu-id="80c39-109">Dieser Befehl speichert die Änderungen, indem ein Commit mit dem aktuellen Konfigurations-Snapshot für die angegebene Verzweigung im Repository erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="80c39-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="80c39-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80c39-110">PARAMETERS</span></span>

### <span data-ttu-id="80c39-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="80c39-111">-Branch</span></span>
<span data-ttu-id="80c39-112">Gibt den Namen der git-Verzweigung an, in der der aktuelle Konfigurations-Snapshot übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="80c39-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="80c39-113">-Context</span><span class="sxs-lookup"><span data-stu-id="80c39-113">-Context</span></span>
<span data-ttu-id="80c39-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="80c39-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="80c39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80c39-115">-DefaultProfile</span></span>
<span data-ttu-id="80c39-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80c39-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80c39-117">-Force</span><span class="sxs-lookup"><span data-stu-id="80c39-117">-Force</span></span>
<span data-ttu-id="80c39-118">Gibt an, dass dieses Cmdlet die aktuelle Konfigurationsdatenbank an das git-Repository übergibt, selbst wenn das git-Repository neuere Änderungen enthält, die überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="80c39-118">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="80c39-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80c39-119">-PassThru</span></span>
<span data-ttu-id="80c39-120">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="80c39-120">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="80c39-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="80c39-121">-Confirm</span></span>
<span data-ttu-id="80c39-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="80c39-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80c39-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80c39-123">-WhatIf</span></span>
<span data-ttu-id="80c39-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="80c39-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80c39-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80c39-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80c39-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80c39-126">CommonParameters</span></span>
<span data-ttu-id="80c39-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80c39-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80c39-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80c39-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80c39-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80c39-129">INPUTS</span></span>

### <span data-ttu-id="80c39-130">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80c39-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80c39-131">System. String</span><span class="sxs-lookup"><span data-stu-id="80c39-131">System.String</span></span>

### <span data-ttu-id="80c39-132">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="80c39-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="80c39-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80c39-133">OUTPUTS</span></span>

### <span data-ttu-id="80c39-134">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="80c39-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="80c39-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="80c39-135">NOTES</span></span>

## <span data-ttu-id="80c39-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80c39-136">RELATED LINKS</span></span>

[<span data-ttu-id="80c39-137">Publish-AzApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="80c39-137">Publish-AzApiManagementTenantGitConfiguration</span></span>](./Publish-AzApiManagementTenantGitConfiguration.md)


