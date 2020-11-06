---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6221C40F-63FC-4D66-B6BD-01024AFF3B65
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Save-AzureRmApiManagementTenantGitConfiguration.md
ms.openlocfilehash: 91cd7855b832a406fdd3ce9a959135936ee3c284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503297"
---
# <span data-ttu-id="3c561-101">Save-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c561-101">Save-AzureRmApiManagementTenantGitConfiguration</span></span>

## <span data-ttu-id="3c561-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c561-102">SYNOPSIS</span></span>
<span data-ttu-id="3c561-103">Speichert Änderungen, indem ein Commit für die aktuelle Konfiguration erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c561-103">Saves changes by creating a commit for current configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c561-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c561-104">SYNTAX</span></span>

```
Save-AzureRmApiManagementTenantGitConfiguration -Context <PsApiManagementContext> -Branch <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c561-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c561-105">DESCRIPTION</span></span>
<span data-ttu-id="3c561-106">Das Cmdlet **Save-AzureRmApiManagementTenantGitConfiguration** speichert die Änderungen durch Erstellen eines Commits, der den aktuellen Konfigurations-Snapshot für eine Verzweigung im Repository enthält.</span><span class="sxs-lookup"><span data-stu-id="3c561-106">The **Save-AzureRmApiManagementTenantGitConfiguration** cmdlet saves the changes by creating a commit that contains the current configuration snapshot to a branch in the repository.</span></span>

## <span data-ttu-id="3c561-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c561-107">EXAMPLES</span></span>

### <span data-ttu-id="3c561-108">Beispiel 1: Speichern von Änderungen an der Konfiguration</span><span class="sxs-lookup"><span data-stu-id="3c561-108">Example 1: Save changes to configuration</span></span>
```
PS C:\>Save-AzureRmApiManagementTenantGitConfiguration -Context $ApimContext -Branch 'master' -PassThru
```

<span data-ttu-id="3c561-109">Dieser Befehl speichert die Änderungen, indem ein Commit mit dem aktuellen Konfigurations-Snapshot für die angegebene Verzweigung im Repository erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c561-109">This command saves the changes by creating a commit with the current configuration snapshot to the specified branch in the repository.</span></span>

## <span data-ttu-id="3c561-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c561-110">PARAMETERS</span></span>

### <span data-ttu-id="3c561-111">-Branch</span><span class="sxs-lookup"><span data-stu-id="3c561-111">-Branch</span></span>
<span data-ttu-id="3c561-112">Gibt den Namen der git-Verzweigung an, in der der aktuelle Konfigurations-Snapshot übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c561-112">Specifies the name of the Git branch in which to commit the current configuration snapshot.</span></span>

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

### <span data-ttu-id="3c561-113">-Context</span><span class="sxs-lookup"><span data-stu-id="3c561-113">-Context</span></span>
<span data-ttu-id="3c561-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3c561-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="3c561-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3c561-115">-Force</span></span>
<span data-ttu-id="3c561-116">Gibt an, dass dieses Cmdlet die aktuelle Konfigurationsdatenbank an das git-Repository übergibt, selbst wenn das git-Repository neuere Änderungen enthält, die überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="3c561-116">Specifies that this cmdlet commits the current configuration database to the Git repository, even if the Git repository has newer changes that are overwritten.</span></span>

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

### <span data-ttu-id="3c561-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c561-117">-PassThru</span></span>
<span data-ttu-id="3c561-118">Gibt an, dass dieses Cmdlet ein **PsApiManagementOperationResult** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3c561-118">Indicates that this cmdlet returns a **PsApiManagementOperationResult** object.</span></span>

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

### <span data-ttu-id="3c561-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c561-119">-Confirm</span></span>
<span data-ttu-id="3c561-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c561-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c561-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c561-121">-WhatIf</span></span>
<span data-ttu-id="3c561-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c561-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c561-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c561-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c561-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c561-124">-DefaultProfile</span></span>
<span data-ttu-id="3c561-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c561-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c561-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c561-126">CommonParameters</span></span>
<span data-ttu-id="3c561-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c561-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c561-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c561-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c561-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c561-129">INPUTS</span></span>

## <span data-ttu-id="3c561-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c561-130">OUTPUTS</span></span>

### <span data-ttu-id="3c561-131">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementOperationResult</span><span class="sxs-lookup"><span data-stu-id="3c561-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperationResult</span></span>

## <span data-ttu-id="3c561-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c561-132">NOTES</span></span>

## <span data-ttu-id="3c561-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c561-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c561-134">Publish-AzureRmApiManagementTenantGitConfiguration</span><span class="sxs-lookup"><span data-stu-id="3c561-134">Publish-AzureRmApiManagementTenantGitConfiguration</span></span>](./Publish-AzureRmApiManagementTenantGitConfiguration.md)


