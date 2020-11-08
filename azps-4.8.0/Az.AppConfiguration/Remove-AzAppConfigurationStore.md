---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173935"
---
# <span data-ttu-id="71662-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="71662-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="71662-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="71662-102">SYNOPSIS</span></span>
<span data-ttu-id="71662-103">Löscht einen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="71662-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="71662-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="71662-104">SYNTAX</span></span>

### <span data-ttu-id="71662-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="71662-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71662-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71662-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71662-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="71662-107">DESCRIPTION</span></span>
<span data-ttu-id="71662-108">Löscht einen Konfigurationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="71662-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="71662-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="71662-109">EXAMPLES</span></span>

### <span data-ttu-id="71662-110">Beispiel 1: Entfernen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="71662-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="71662-111">Mit diesem Befehl wird ein App-Konfigurationsspeicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="71662-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="71662-112">Beispiel 2: Entfernen eines App-Konfigurationsspeichers</span><span class="sxs-lookup"><span data-stu-id="71662-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="71662-113">Mit diesem Befehl wird ein App-Konfigurationsspeicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="71662-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="71662-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="71662-114">PARAMETERS</span></span>

### <span data-ttu-id="71662-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71662-115">-AsJob</span></span>
<span data-ttu-id="71662-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="71662-116">Run the command as a job</span></span>

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

### <span data-ttu-id="71662-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71662-117">-DefaultProfile</span></span>
<span data-ttu-id="71662-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="71662-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71662-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="71662-119">-InputObject</span></span>
<span data-ttu-id="71662-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="71662-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71662-121">-Name</span><span class="sxs-lookup"><span data-stu-id="71662-121">-Name</span></span>
<span data-ttu-id="71662-122">Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="71662-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71662-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="71662-123">-NoWait</span></span>
<span data-ttu-id="71662-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="71662-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71662-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71662-125">-PassThru</span></span>
<span data-ttu-id="71662-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="71662-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="71662-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71662-127">-ResourceGroupName</span></span>
<span data-ttu-id="71662-128">Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="71662-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71662-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="71662-129">-SubscriptionId</span></span>
<span data-ttu-id="71662-130">Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="71662-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71662-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="71662-131">-Confirm</span></span>
<span data-ttu-id="71662-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="71662-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71662-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71662-133">-WhatIf</span></span>
<span data-ttu-id="71662-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="71662-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71662-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="71662-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71662-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71662-136">CommonParameters</span></span>
<span data-ttu-id="71662-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71662-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71662-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71662-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71662-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="71662-139">INPUTS</span></span>

### <span data-ttu-id="71662-140">Microsoft. Azure. PowerShell. Cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="71662-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="71662-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="71662-141">OUTPUTS</span></span>

### <span data-ttu-id="71662-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="71662-142">System.Boolean</span></span>

## <span data-ttu-id="71662-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="71662-143">NOTES</span></span>

<span data-ttu-id="71662-144">Aliase</span><span class="sxs-lookup"><span data-stu-id="71662-144">ALIASES</span></span>

<span data-ttu-id="71662-145">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71662-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71662-146">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="71662-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71662-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="71662-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71662-148">Inputobject <IAppConfigurationIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="71662-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71662-149">`[ConfigStoreName <String>]`: Der Name des Konfigurationsspeichers.</span><span class="sxs-lookup"><span data-stu-id="71662-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="71662-150">`[GroupName <String>]`: Der Name der privaten Link Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="71662-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="71662-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="71662-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71662-152">`[PrivateEndpointConnectionName <String>]`: Privater Endpunkt-Verbindungsname</span><span class="sxs-lookup"><span data-stu-id="71662-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="71662-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Container Registrierung gehört.</span><span class="sxs-lookup"><span data-stu-id="71662-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="71662-154">`[SubscriptionId <String>]`: Die Microsoft Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="71662-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="71662-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="71662-155">RELATED LINKS</span></span>

